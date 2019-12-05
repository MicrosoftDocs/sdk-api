---
UID: NN:mmc.INodeProperties
title: INodeProperties (mmc.h)
description: The INodeProperties interface retrieves text-only properties for a node.
old-location: mmc\inodeproperties.htm
tech.root: mmc
ms.assetid: 5ef78fb9-704e-4c1d-ada8-c257a0944c94
ms.date: 12/05/2018
ms.keywords: INodeProperties, INodeProperties interface [MMC], INodeProperties interface [MMC],described, _slate_inodeproperties, mmc.inodeproperties, mmc/INodeProperties
ms.topic: interface
f1_keywords:
- mmc/INodeProperties
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmc.h
api_name:
- INodeProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INodeProperties interface


## -description


The 
<b>INodeProperties</b> interface retrieves text-only properties for a node. This interface is implemented by snap-ins and its methods are called by the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-the-extended-view-extension">Extended View</a> extension that ships with MMC 2.0. Other view extensions and the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a> (particularly the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/node-object">Node</a>) can also use the 
<b>INodeProperties</b> interface.

The 
<b>INodeProperties</b> interface is queried (using 
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>) from the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface for scope nodes, and from the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface for result items.

The Extended View extension queries two properties, CCF_DESCRIPTION and CCF_HTML_DETAILS. Instead of implementing 
<b>INodeProperties</b>, a snap-in can return values for these properties through data-object clipboard formats. The 
<b>INodeProperties</b> interface is available to snap-in developers whose data objects may not readily provide the property values.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INodeProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INodeProperties</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-inodeproperties-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves text-only properties for a node. Text-only properties are exposed in the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/node-object">Node object</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/ccf-description">CCF_DESCRIPTION clipboard format</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/ccf-html-details">CCF_HTML_DETAILS clipboard format</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/node-object">Node object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/node-property">Node.Property</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-the-extended-view-extension">Using the Extended View Extension</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-the-extended-view-extension-implementation-details">Using the Extended View Extension - Implementation Details</a>
 

 

