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

# IUPnPDescriptionDocument interface


## -description


The 
<b>IUPnPDescriptionDocument</b> interface enables an application to load a device description.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDescriptionDocument</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IUPnPDescriptionDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUPnPDescriptionDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26f5a7f0-7d29-47a6-9f43-6b0d921342ae">Abort</a>
</td>
<td align="left" width="63%">
Stops an asynchronous load operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f8ae379-3ec6-4fe2-ae7b-fe3750a5d4c3">DeviceByUDN</a>
</td>
<td align="left" width="63%">
Returns a device from the currently loaded document with the specified unique device name (UDN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ae8af2-44f2-4b7c-a426-f2a26c43da37">Load</a>
</td>
<td align="left" width="63%">
Loads a document synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">LoadAsync</a>
</td>
<td align="left" width="63%">
Loads a document asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406413">RootDevice</a>
</td>
<td align="left" width="63%">
Returns the root device of the loaded document's device tree.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDescriptionDocument</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3faf3dfa-ed42-4dbd-9ad7-7e34a8b00be8">LoadResult</a>


</td>
<td align="left" width="63%">
Result code that indicates the success or failure of a completed load operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/592939fa-ebce-419f-a813-ecbbe788fd8e">ReadyState</a>


</td>
<td align="left" width="63%">
Status of the document load operation.

</td>
</tr>
</table> 

