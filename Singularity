BootStrap: shub
From: shub://willgpaik/centos7_aci:latest

%setup

%files

%environment 
  export PATH=$PATH:/opt/sw/allpaths/bin

%runscript


%post
  yum -y update

  mkdir -p /opt/sw/allpaths
  cd /opt/sw
  wget ftp://ftp.broadinstitute.org/pub/crd/ALLPATHS/Release-LG/latest_source_code/LATEST_VERSION.tar.gz
  tar -xf LATEST_VERSION.tar.gz
  cd allpathslg-52488
  ./configure --prefix=/opt/sw/allpaths
  make
  make install
  
  cd /opt/sw
  rm -rf allpathslg-52488
  rm LATEST_VERSION.tar.gz
