BootStrap: shub
From: shub://willgpaik/centos7_aci:latest
%setup

%files

%environment 
    PATH="$PATH:/usr/lib64/openmpi/bin/:/opt/sw/freefem/bin/"
    export PATH

%runscript


%post
    yum -y install m4-devel \
      bison-devel \
      flex-devel \
      patch \
      openmpi-devel \
      fftw-devel \
      openblas-devel \
      lapack-devel \
      freeglut-devel \
      scotch-devel \
      arpack-devel \
      suitesparse-devel \
      MUMPS-devel \
      NLopt-devel \
      coin-or-Ipopt-devel \
      gnuplot
    yum -y update

    source /opt/rh/devtoolset-8/enable

    # Install FreeFem++
    mkdir -p /opt/sw/
    cd /opt/
    wget https://raw.githubusercontent.com/willgpaik/freefem_aci/master/freefem_install.sh
    chmod +x freefem_install.sh
    ./freefem_install.sh
    
    rm freefem_install.sh
