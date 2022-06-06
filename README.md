---
description: 概述
---

# 概述

Linkerd 是 Kubernetes 的服务网格。 它通过为您提供运行时调试、可观察性、可靠性和安全性，使运行服务更容易、更安全——所有这些都不需要对您的代码进行任何更改。

有关服务网格模型的简要介绍，我们建议阅读[服务网格：每个软件工程师需要了解的关于世界上最热门的技术。](https://servicemesh.io/)

Linkerd 是完全开源的，使用[ Apache v2 ](https://github.com/linkerd/linkerd2/blob/main/LICENSE)开源许可证，是一个[CNCF云原生基金会](https://cncf.io/)毕业的项目。 Linkerd 在[ Linkerd GitHub ](https://github.com/linkerd)组织进行公开发行。

Linkerd 具有三个基本组件：UI、数据平面和控制平面。 您通过以下方式运行 Linkerd：

1. [在本地系统上安装 CLI](https://linkerd.io/2.11/getting-started/#step-1-install-the-cli)
2. [将控制平面安装到集群中](https://linkerd.io/2.11/getting-started/#step-3-install-linkerd-onto-the-cluster)
3. [将您的服务添加到 Linkerd 的数据平面](https://linkerd.io/2.11/tasks/adding-your-service/)

当一个服务基于Linkerd运行后，您可以使用 [Linkerd  UI](https://linkerd.io/2.11/getting-started/#step-4-explore-linkerd%E2%80%98) 来检查和操作它。

[马上开始！](https://linkerd.io/2.11/getting-started/)

### Linkerd是如何工作的?

Linkerd 通过在每个服务实例旁边安装一组超轻、透明的代理来工作。 这些代理会自动处理进出服务的所有流量。 因为它们是透明的，所以这些代理充当高度仪表化的进程外网络堆栈，向控制平面发送遥测数据并从控制平面接收控制信号。 这种设计允许 Linkerd 测量和操纵进出您的服务的流量，而不会引入过多的延迟。

为了尽可能小、轻量和安全，Linkerd 的代理是用 [Rust ](https://www.rust-lang.org/)编写的，专门用于 Linkerd。 您可以在[ Linkerd 代理存储库](https://github.com/linkerd/linkerd2-proxy)中了解有关代理的更多信息。

