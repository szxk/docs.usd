---
layout: default
title: USD介绍
nav_order: 1
description: ""
permalink: /
---

# USD介绍
{: .no_toc }

---
![](https://graphics.pixar.com/usd/docs/attachments/340328893/553309696.jpg)

1. TOC
{:toc}

## 什么是USD?
---
在CG电影以及游戏领域，通常需要搭建能够生成、保存并能够传输大量3D数据的管线，我们称之为“场景描述（Scene Description）”。为了应对不同的需求以及工作流程，一个生产管线中所参与的应用程序（建模、着色、动画、灯光、特效、渲染）通常各自都有专门的场景描述形式，而且无法通过其它应用程序读取与编辑。通用场景描述(USD)是第一款旨在提供稳定且可扩展的3D数据交换与编辑功能的开源工具集，针对包含大量基本元素的场景提供了更加通用的描述形式。

USD提供了最基本的元素资产（像是模型）或者动画的数据交换功能。但是跟其它的数据格式不同的是，USD能够将任意数量的资产组装并整合在虚拟集合、场景或者镜头中，之后可以在不同的应用程序之间传输这些数据，在单独的场景图表中调用简单一致的API进行无损编辑（如覆盖）的操作。USD提供了丰富的工具集用于读取、写入、编辑以及快速预览3D几何体和材质着色。此外，由于USD的核心概念——场景图表和“合成引擎”与3D无关，因此USD能够以一种可维护的方式进行扩展，从而对其它领域的数据进行编码与合成。

## 为什么使用USD?
---
USD是皮克斯3D图形管线的核心，被使用在每个3D制作和渲染应用程序中，包括皮克斯专有的Presto动画系统。
皮克斯致力于发展和改进USD以满足下列生产需求：
- **为定义、打包、组合与编辑3D数据提供丰富且通用的语言，便于在多种数字内容制作软件中使用。**和许多其它形式的数据包一样，USD提供了底层数据模型，在“数据格式层级”上规定了数据的编码与组织形式，外加一组（可扩展）高级架构，为[Mesh](https://graphics.pixar.com/usd/docs/api/class_usd_geom_mesh.html#details)和[Transform](https://graphics.pixar.com/usd/docs/api/class_usd_geom_xformable.html#details)等概念提供了合理高效的API和组织形式。有了这样的基础就可以创建几何与着色缓存。但是USD进一步提供了一组叫“[合成弧](https://graphics.pixar.com/usd/docs/USD-Glossary.html#USDGlossary-CompositionArcs)”的工具，用于打包、聚合、生成变体与覆盖Primitive元素和资产，配合高性能的运行时引擎生成称为“[舞台（Stage）](https://graphics.pixar.com/usd/docs/USD-Glossary.html#USDGlossary-Composition)”的场景图表，进而解析“[合成的场景描述](https://graphics.pixar.com/usd/docs/USD-Glossary.html#USDGlossary-Composition)”的结果并从中提取数据。

- **允许多个艺术家在同一资产和场景上进行协作。**USD中用来对子层进行操作的合成弧，让每个艺术家只需要在自己的文件（或者叫[层](https://graphics.pixar.com/usd/docs/USD-Glossary.html#USDGlossary-Layer)Layer）中工作，从而方便不同部门或同一部门内的多个艺术家同时处理相同的资产或场景，最后这些层都能够按照各自USD文件中定义的优先级进行合并与解析。当然这并不是说在建模师修改一个优先级较低模型的拓扑结构时，优先级较高的层能够自动调整着色数据，USD流程是要让每个艺术家能够独立工作，无需覆盖或修改其他艺术家的工作内容，同时它也能够提供清晰的变更审计跟踪，有助于解决诸如上述拓扑变化问题之类的问题。

- **尽可能地降低延迟从而得到最优化的艺术内容迭代效率。**在多数数字媒体领域，对于实现高质量数字艺术内容的最重要的条件

## USD能做什么?
---

## USD不能做什么?
---

## USD在皮克斯的发展
---

## 更多USD资源
---

