## Setup and installation:

### Basic Requirements:
* [.NET Core SDK](https://www.microsoft.com/net/download/core)
* [Git for Windows](https://git-scm.com/)
* [Visual Studio Code](https://code.visualstudio.com/) with C# and Docker extensions
* [Visual Studio 2017 CE](https://www.visualstudio.com/free-developer-offers/)
* [Docker CE](https://www.docker.com/community-edition#/download)
* Start docker and execute ``./pull.sh``

### Optional Requirements:
* [.NET Portability Analyzer](http://vsixgallery.com/extension/55d15546-28ca-40dc-af23-dfa503e9c5fe/)
* [MSBuild StructuredLog](https://github.com/KirillOsenkov/MSBuildStructuredLog)
* [ILSpy](http://ilspy.net/)

### Local Kubernetes with **minikube**
* Install [**chocolatey**](https://chocolatey.org/)
* Install [**minikube**](https://github.com/kubernetes/minikube) and [**Helm**](https://github.com/kubernetes/helm)   
    ```bash
    choco install minikube
    choco install kubernetes-helm
    ```
* Start **minikube** [**with hyperV**](https://medium.com/@JockDaRock/minikube-on-windows-10-with-hyper-v-6ef0f4dc158c) 
    ```powershell
    minikube start --bootstrapper=kubeadm --vm-driver="hyperv" --memory=4096 --cpus=2 --hyperv-virtual-switch="<name of the created virtual switch>"
    ```
* Connect to minikube docker engine  ``./minikube-docker.ps1``
* Pull docker images inside minikube executing ``./pull.sh``