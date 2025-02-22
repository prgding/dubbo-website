---
aliases:
    - /zh/overview/what/
description: ""
hide_summary: true
linkTitle: 介绍
no_list: true
title: Dubbo 介绍
type: docs
weight: 3
---


[5 分钟快速掌握 Apache Dubbo]({{< relref "../../blog/news/dubbo-introduction" >}})

Apache Dubbo 是一款 RPC 服务开发框架，用于解决微服务架构下的服务治理与通信问题，官方提供了 Java、Golang 等多语言 SDK 实现。使用 Dubbo 开发的微服务原生具备相互之间的远程地址发现与通信能力，
利用 Dubbo 提供的丰富服务治理特性，可以实现诸如服务发现、负载均衡、流量调度等服务治理诉求。Dubbo 被设计为高度可扩展，用户可以方便的实现流量拦截、选址的各种定制逻辑。

在云原生时代，Dubbo 相继衍生出了 Dubbo3、Proxyless Mesh 等架构与解决方案，在易用性、超大规模微服务实践、云原生基础设施适配、安全性等几大方向上进行了全面升级。

## Dubbo 的开源故事

Apache Dubbo 最初是为了解决阿里巴巴内部的微服务架构问题而设计并开发的，在十多年的时间里，它在阿里巴巴公司内部的很多业务系统的到了非常广泛的应用。最早在 2008 年，阿里巴巴就将 Dubbo 捐献到开源社区，它很快成为了国内开源服务框架选型的事实标准框架，得到了业界更广泛的应用。在 2017 年，Dubbo 被正式捐献 Apache 软件基金会并成为 Apache 顶级项目，开始了一段新的征程。

Dubbo 被证实能很好的满足企业的大规模微服务实践，并且能有效降低微服务建设的开发与管理成本，不论是阿里巴巴还是工商银行、中国平安、携程、海尔等社区用户，它们都通过多年的大规模生产环境流量对 Dubbo 的稳定性与性能进行了充分验证。后来 Dubbo 在很多大企业内部衍生出了独立版本，比如在阿里巴巴内部就基于 Dubbo 衍生出了 HSF，HSF 见证了阿里巴巴以电商业务为首的微服务系统的快速发展。自云原生概念推广以来，各大厂商都开始拥抱开源标准实现，阿里巴巴将其内部 HSF 系统与开源社区 Dubbo 相融合，与社区一同推出了云原生时代的 Dubbo3 架构，截止 2022 年双十一结束，**Dubbo3 已经在阿里巴巴内部全面取代 HSF 系统，包括电商核心、阿里云等核心系统已经全面运行在 Dubbo3 之上**。

## 为什么需要 Dubbo，它能做什么？
按照微服务架构的定义，采用它的组织能够很好的提高业务迭代效率与系统稳定性，但前提是要先能保证微服务按照期望的方式运行，要做到这一点需要解决服务拆分与定义、数据通信、地址发现、流量管理、数据一致性、系统容错能力等一系列问题。

Dubbo 可以帮助解决如下微服务实践问题：

* **微服务编程范式和工具**

Dubbo 支持基于 IDL 或语言特定方式的服务定义，提供多种形式的服务调用形式（如同步、异步、流式等）

* **高性能的 RPC 通信**

Dubbo 帮助解决微服务组件之间的通信问题，提供了基于 HTTP、HTTP/2、TCP 等的多种高性能通信协议实现，并支持序列化协议扩展，在实现上解决网络连接管理、数据传输等基础问题。

* **微服务监控与治理**

Dubbo 官方提供的服务发现、动态配置、负载均衡、流量路由等基础组件可以很好的帮助解决微服务基础实践的问题。除此之外，您还可以用 Admin 控制台监控微服务状态，通过周边生态完成限流降级、数据一致性、链路追踪等能力。

* **部署在多种环境**

Dubbo 服务可以直接部署在容器、Kubernetes、Service Mesh等多种架构下。

* **活跃的社区**

Dubbo 项目托管在 Apache 社区，有来自国际、国内的活跃贡献者维护着超 10 个生态项目，贡献者包括来自海外、阿里巴巴、工商银行、携程、蚂蚁、腾讯等知名企业技术专家，确保 Dubbo 及时解决项目缺陷、需求及安全漏洞，跟进业界最新技术发展趋势。

* **庞大的用户群体**

Dubbo3 已在阿里巴巴成功取代 HSF 框架实现全面落地，成为阿里集团面向云原生时代的统一服务框架，庞大的用户群体是 Dubbo 保持稳定性、需求来源、先进性的基础。

## Dubbo 不是什么？

* **不是应用开发框架的替代者**

Dubbo 设计为让开发者以主流的应用开发框架的开发模式工作，它不是各个语言应用开发框架的替代者，如它不是 Spring/Spring Boot 的竞争者，当你使用 Spring 时，Dubbo 可以无缝的与 Spring & Spring Boot 集成在一起。

* **不仅仅只是一款 RPC 框架**

Dubbo 提供了内置 RPC 通信协议实现，但它不仅仅是一款 RPC 框架。首先，它不绑定某一个具体的 RPC 协议，开发者可以在基于 Dubbo 开发的微服务体系中使用多种通信协议；其次，除了 RPC 通信之外，Dubbo 提供了丰富的服务治理能力与生态。

* **不是 gRPC 协议的替代品**

Dubbo 支持基于 gRPC 作为底层通信协议，在 Dubbo 模式下使用 gRPC 可以带来更好的开发体验，享有统一的编程模型和更低的服务治理接入成本

* **不只有 Java 语言实现**

自 Dubbo3 开始，Dubbo 提供了 Java、Golang、Rust、Node.js 等多语言实现，未来会有更多的语言实现。
