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

# IWICMetadataReaderInfo interface


## -description


Exposes methods that provide basic information about the registered metadata reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataReaderInfo</b> interface inherits from <a href="https://msdn.microsoft.com/505105c2-de50-4b5f-9089-e9a3cea2f464">IWICMetadataHandlerInfo</a>. <b>IWICMetadataReaderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataReaderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6ee4ee9-8d9d-44f7-aab8-8e8ccfa7f942">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc0033f7-801d-4ae0-a2cb-bdda25303476">GetPatterns</a>
</td>
<td align="left" width="63%">
Gets the metadata patterns associated with the metadata reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58ac58f4-25e0-4fc4-8d2a-854bb89e4af6">MatchesPattern</a>
</td>
<td align="left" width="63%">
Determines if a stream contains a metadata item pattern.

</td>
</tr>
</table> 

