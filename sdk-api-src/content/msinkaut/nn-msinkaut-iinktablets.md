---
UID: NN:msinkaut.IInkTablets
title: IInkTablets
author: windows-sdk-content
description: "."
old-location: tablet\iinktablets.htm
tech.root: tablet
ms.assetid: 98052ECB-9385-45C9-A03C-3F312ADD9872
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkTablets, IInkTablets interface [Tablet PC], IInkTablets interface [Tablet PC],described, msinkaut/IInkTablets, tablet.iinktablets
ms.topic: interface
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - msinkaut.h
api_name:
 - IInkTablets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkTablets interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablets</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkTablets</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkTablets</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f83caf4a-b8ca-4cee-9060-679128a1bd77">IsPacketPropertySupported</a>
</td>
<td align="left" width="63%">
Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. For example, use this method to determine if all of the tablets in a collection support tangential pressure from a pen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ead8bd-9f96-4862-b9b4-b1f3def1efa6">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object at the specified index within the <a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTablets</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6224871c-044e-478a-9635-6b2874bdcf45">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of objects or collections contained in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4a9713c6-91a0-4632-9c8d-58d5e1b98478">DefaultTablet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the default tablet within the set of available tablets.

</td>
</tr>
</table> 

