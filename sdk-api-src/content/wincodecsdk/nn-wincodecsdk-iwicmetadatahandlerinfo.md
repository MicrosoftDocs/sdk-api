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

# IWICMetadataHandlerInfo interface


## -description


Exposes methods that provide basic information about the registered metadata handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataHandlerInfo</b> interface inherits from <a href="https://msdn.microsoft.com/a31267ed-60cd-4de9-9fed-26bb390b29e6">IWICComponentInfo</a>. <b>IWICMetadataHandlerInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataHandlerInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/522294c5-e424-40cf-b982-275198e705dc">DoesRequireFixedSize</a>
</td>
<td align="left" width="63%">
Determines if the metadata handler requires a fixed size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f434fd44-47a2-40be-ab3f-3d99b5e0e56a">DoesRequireFullStream</a>
</td>
<td align="left" width="63%">
Determines if the handler requires a full stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93f4e77a-52e3-47c7-9c48-9d38a2c8ceba">DoesSupportPadding</a>
</td>
<td align="left" width="63%">
Determines if the metadata handler supports padding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46d5246d-4ef5-457c-b36b-68e0f956952b">GetContainerFormats</a>
</td>
<td align="left" width="63%">
Retrieves the container formats supported by the metadata handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab3cd583-055d-4414-a615-600e4c67dcc4">GetDeviceManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the device manufacturer of the metadata handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ab47616-8097-441f-9d8e-6f1518246759">GetDeviceModels</a>
</td>
<td align="left" width="63%">
Retrieves the device models that support the metadata handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a54d59a-3fe4-4636-94a0-5ee449d1d5c3">GetMetadataFormat</a>
</td>
<td align="left" width="63%">
Retrieves the metadata format of the metadata handler.

</td>
</tr>
</table> 

