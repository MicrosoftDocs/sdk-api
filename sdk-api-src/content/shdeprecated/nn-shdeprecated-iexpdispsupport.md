---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IExpDispSupport interface


## -description


Deprecated. Exposes methods that allow the retrieval of properties, translation of keyboard accelerators, and determination of a connection point for certain events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExpDispSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExpDispSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExpDispSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef8d4e8c-7f85-4920-b149-1bf277d3fd5e">FindCIE4ConnectionPoint</a>
</td>
<td align="left" width="63%">
Deprecated. Gets connection points for browser events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92228340-2472-4920-90b7-ce46cab7406e">OnInvoke</a>
</td>
<td align="left" width="63%">
Deprecated. Gets ambient properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55f3b4dd-134d-49fe-a7f7-c6315971e902">OnTranslateAccelerator</a>
</td>
<td align="left" width="63%">
Deprecated. Instructs the control site to process the keystroke described in <i>pMsg</i> and modified by the flags in <i>grfModifiers</i>.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  <b>IExpDispSupport</b> might not be supported in versions of Windows later than Windows XP.</div>
<div> </div>


