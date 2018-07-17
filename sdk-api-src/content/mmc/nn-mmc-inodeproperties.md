---
UID: NN:mmc.INodeProperties
title: INodeProperties
author: windows-sdk-content
description: The INodeProperties interface retrieves text-only properties for a node.
old-location: mmc\inodeproperties.htm
old-project: mmc
ms.assetid: 5ef78fb9-704e-4c1d-ada8-c257a0944c94
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: INodeProperties, INodeProperties interface [MMC], INodeProperties interface [MMC],described, _slate_inodeproperties, mmc.inodeproperties, mmc/INodeProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - INodeProperties
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# INodeProperties interface


## -description


The 
<b>INodeProperties</b> interface retrieves text-only properties for a node. This interface is implemented by snap-ins and its methods are called by the 
<a href="https://msdn.microsoft.com/56fa12d4-a804-468f-9df5-7b0db786f79f">Extended View</a> extension that ships with MMC 2.0. Other view extensions and the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a> (particularly the 
<a href="https://msdn.microsoft.com/c504cb3f-8ec6-49fe-b0d3-05ea9cad61f4">Node</a>) can also use the 
<b>INodeProperties</b> interface.

The 
<b>INodeProperties</b> interface is queried (using 
<a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a>) from the 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface for scope nodes, and from the 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> interface for result items.

The Extended View extension queries two properties, CCF_DESCRIPTION and CCF_HTML_DETAILS. Instead of implementing 
<b>INodeProperties</b>, a snap-in can return values for these properties through data-object clipboard formats. The 
<b>INodeProperties</b> interface is available to snap-in developers whose data objects may not readily provide the property values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INodeProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INodeProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INodeProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e891428a-c0a1-4451-aa69-c0a4a3d09078">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves text-only properties for a node. Text-only properties are exposed in the 
<a href="https://msdn.microsoft.com/c504cb3f-8ec6-49fe-b0d3-05ea9cad61f4">Node object</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/eff5b42b-662a-49b0-bc32-9522e7c12704">CCF_DESCRIPTION clipboard format</a>



<a href="https://msdn.microsoft.com/608826eb-e0ae-423c-98ed-4519d77e6d84">CCF_HTML_DETAILS clipboard format</a>



<a href="https://msdn.microsoft.com/c504cb3f-8ec6-49fe-b0d3-05ea9cad61f4">Node object</a>



<a href="https://msdn.microsoft.com/edb52d1b-e422-4c94-9462-7dca2f15b231">Node.Property</a>



<a href="https://msdn.microsoft.com/56fa12d4-a804-468f-9df5-7b0db786f79f">Using the Extended View Extension</a>



<a href="https://msdn.microsoft.com/e43f03c3-b0ef-43df-ac7a-9fa9aeea8b92">Using the Extended View Extension - Implementation Details</a>
 

 

