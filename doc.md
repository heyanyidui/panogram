## 项目目录文档

由于该开源项目并没有提供足够多的文档，所以为了进一步开发，这里总结一下项目目录结构。

因为主要使用 canvas 进行相关绘制，所以核心应该是关注 js 文件。

### js

* AbstractHoverbox： 抽象类，对所有元素的抽象，重点关注以下参数。

  * @class AbstractHoverbox

  * @constructor

  * @param {AbstractNode} node The node Person or Partnership for which the hoverbox is drawn

  * @param {Number} x The x coordinate for the hoverbox

  * @param {Number} y The y coordinate for the hoverbox

  * @param {Number} width The width in pixels

  * @param {Number} height The height in pixels

  * @param {Number} nodeX The x coordinate of the node for which the hoverbox is drawn

  * @param {Number} nodeY The y coordinate of the node for which the hoverbox is drawn

  * @param {Raphael.st} nodeShapes Raphaël set containing the graphical elements that make up the node

* AbstractNode：抽象类，结点。每个结点包含它的位置信息和与其他结点之间的关系。

  * @class AbstractNode

  * @constructor

  * @param {Number} x The x coordinate on the canvas

  * @param {Number} y The y coordinate on the canvas

  * @param {Number} [id] The id of the node

* AbstractNodeVisuals： 抽象类，Pedigree用到的通用图像引擎抽象类。

  * @class AbstractNodeVisuals

  * @constructor

  * @param {AbstractNode} node The node for which the graphics are drawn

  * @param {Number} x The x coordinate on the canvas

  * @param {Number} y The y coordinate on the canvas

* AbstractPerson： 继承 AbstractNode的抽象类，用户结点。

  * @param {Number} x The x coordinate on the canvas

  * @param {Number} y The y coordinate on the canvas

  * @param {String} gender Can be "M", "F", or "U"

  * @param {Number} [id] The id of the node

* AbstractPersonVisuals：继承 AbstractNodeVisuals

  * @param {AbstractPerson} node The node for which this graphics are handled

  * @param {Number} x The x coordinate on the canvas

  * @param {Number} y the y coordinate on the canvas

* actionButtons：压缩后文件

* ageCalc： 根据用户出生日期和死亡日期，返回用户年龄。

* BaseGraph： 将系谱树表示为节点和边的图形，这些节点和边都附加了某些属性。

* Blob：外部文件

* compatibility：外部文件

* ContentTopMenu： 压缩文件

* controller：控制器（上面菜单）

* DateTimePicker：外部文件

* disorder：一个用于存储遗传性疾病信息并从OMIM数据库加载的类。这些疾病可以归因于家系中的一个人。

* disorderLegend: 负责跟踪疾病及其属性，并缓存从OMIM数据库加载的疾病数据。

* dragdrop：压缩文件
* dynamicGraph： 增加了对在线修改的支持，并为UI实现提供了一个方便的API。
* edgeOptimization：
* effects：压缩文件
* export：导出类
* exportSelector：导出时选择
* FileSaver：保存文件。外部文件。
* fullscreen：压缩文件。
* geneLegend：负责跟踪候选基因的类。
* graphicHelpers：返回一个raphael元素，该元素表示表示给定性别的图标的类似Pi图的部分。
* helper：对不同浏览器的支持。
* hpoLegend：类负责跟踪HPO术语及其属性并缓存从OMIM数据库加载的紊乱数据。
* HPOTerm：存储pheno 类型相关信息等
* html2canvas：外部文件，压缩文件
* import：导入文件。
* importSelector：导入时对应选择。
* legend：用例图的基础类。
* lineSet： LineSet用于跟踪图形中的现有直线，并简化线交叉线跟踪
* livevalidation_prototype：压缩文件。
* lock：压缩文件
* markerScript：压缩文件
* NodeMenu：是一个包含AbstractNode元素选项的UI元素
* nodetypeSelectionBubble：包含用于创建新节点的选项的UI元素（“bubble”）。
* okCancelDialogue：在可移动/半透明对话中向用户显示提示的UI元素
* ordering：
* partnership：表示两个结点之间的关系类。
* PartnershipVisuals：用于可视化合作关系和组织图形元素的类。
* pedigree：该系统的主类，负责初始化应用程序的所有基本元素。

