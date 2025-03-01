<h1>Tutorial to setup standalone Testkube for a K8s cluster & kubectl testkube CLI on Windows</h1>

This tutorial installs Testkube API on a K8s cluster running on Docker Desktop and `kubectl testkube` on a local Windows 10 machine.

TestKube follows a client-server architecture with:
1. __Server-side components__ installed on the Kubernetes cluster:

    - TestKube API server
    - MongoDB (for test storage)
    - NATS (for messaging)
    - MinIO (for artifact storage)
    - Operator (for managing CRDs)
    - Various executors for different test types

   These components are installed with helm-charts.

2. __Client-side component__ on the local machine:

    - kubectl-testkube CLI tool that communicates with the API server

    This component is installed directly from the Github page of the project.

<h2>Installing Testkube server-side components</h2>

Helm must be installed on the local machine to install the Testkube server-side components. On Windows 10, helm can be installed with `winget install Helm.Helm`. 

Check helm installation with `helm version`.

Next, run the following commands to install testkube API components into the K8s cluster using helm-charts. This will install in the `testkube` namespace.

![helm_testkube](https://github.com/Kubelix/Resources/blob/main/helm_testkube.png)

To verify if the Testkube pods have been created in the cluster, run the following:

![testkube_verify](https://github.com/Kubelix/Resources/blob/main/testkube_verify.png)

<h2>Installing Testkube client-side component</h2>

The client-side component is just `kubectl-testkube` CLI which can be installed directly from the official [Github Testkube releases page](https://github.com/kubeshop/testkube/releases).

Make sure to add the `kubectl-testkube.exe` file location to `PATH`.

Verify installation by running the following:

![kubectl_testkube_verify](https://github.com/Kubelix/Resources/blob/main/kubectl_testkube_verify.png)

Point the Testkube CLI to the correct API server:

![kubectl_port_forward](https://github.com/Kubelix/Resources/blob/main/kubectl_port_forward.png)

Verify connection to Testkube server in K8s cluster:

![kubectl_testkube_status](https://github.com/Kubelix/Resources/blob/main/kubectl_testkube_status.png)

<h1>Tutorial to setup standalone Testkube for a K8s cluster & kubectl testkube CLI on Windows</h1>

This tutorial installs Testkube API on a K8s cluster running on Docker Desktop and `kubectl testkube` on a local Windows 10 machine.

TestKube follows a client-server architecture with:
1. __Server-side components__ installed on the Kubernetes cluster:

    - TestKube API server
    - MongoDB (for test storage)
    - NATS (for messaging)
    - MinIO (for artifact storage)
    - Operator (for managing CRDs)
    - Various executors for different test types

   These components are installed with helm-charts.

2. __Client-side component__ on the local machine:

    - kubectl-testkube CLI tool that communicates with the API server

    This component is installed directly from the Github page of the project.

<h2>Installing Testkube server-side components</h2>

Helm must be installed on the local machine to install the Testkube server-side components. On Windows 10, helm can be installed with `winget install Helm.Helm`. 

Check helm installation with `helm version`.

Next, run the following commands to install testkube API components into the K8s cluster using helm-charts. This will install in the `testkube` namespace.

![helm_testkube](https://github.com/Kubelix/Resources/blob/main/helm_testkube.png)

To verify if the Testkube pods have been created in the cluster, run the following:

![testkube_verify](https://github.com/Kubelix/Resources/blob/main/testkube_verify.png)

<h2>Installing Testkube client-side component</h2>

The client-side component is just `kubectl-testkube` CLI which can be installed directly from the official [Github Testkube releases page](https://github.com/kubeshop/testkube/releases).

Make sure to add the `kubectl-testkube.exe` file location to `PATH`.

Verify installation by running the following:

![kubectl_testkube_verify](https://github.com/Kubelix/Resources/blob/main/kubectl_testkube_verify.png)

Point the Testkube CLI to the correct API server:

![kubectl_port_forward](https://github.com/Kubelix/Resources/blob/main/kubectl_port_forward.png)

Verify connection to Testkube server in K8s cluster:

![kubectl_testkube_status](https://github.com/Kubelix/Resources/blob/main/kubectl_testkube_status.png)

This confirms that the API connection is fine but the Telemetry is not sending any usage data, which is fine.

Create a basic test:

![testkube_create_basic_test](https://github.com/Kubelix/Resources/blob/main/testkube_create_basic_test.png)





