FROM ubuntu
RUN apt update -y && apt install -y curl
RUN curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
RUN curl -sSL -o argocd-linux-amd64 https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64 && install -m 555 argocd-linux-amd64 /usr/local/bin/argocd &&  rm argocd-linux-amd64
#RUN curl -L -o vcluster "https://github.com/loft-sh/vcluster/releases/latest/download/vcluster-linux-amd64" && install -c -m 0755 vcluster /usr/local/bin && rm -f vcluster
RUN curl -L -o vcluster "https://github.com/loft-sh/vcluster/releases/download/v0.20.0-beta.12/vcluster-linux-amd64" && install -c -m 0755 vcluster /usr/local/bin && rm -f vcluster
#RUN kubectl version --client && argocd version
