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

# IMetaDataTables2 interface


## -description


Extends <a href="https://msdn.microsoft.com/30d06e87-93a2-4a9c-8843-4c42d7d9e3c8">IMetaDataTables</a> to include methods for working with metadata streams.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataTables2</b> interface inherits from <b>IMetaDataTables</b>. <b>IMetaDataTables2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataTables2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7de4fccb-9cd6-443d-bbd3-ba545e040ca6">GetMetaDataStorage</a>
</td>
<td align="left" width="63%">
Gets the size and contents of the metadata stored in the specified section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a292a32a-b9c2-46b5-a2c4-074e616d7675">GetMetaDataStreamInfo</a>
</td>
<td align="left" width="63%">
Gets the name, size, and contents of the metadata stream at the specified index.

</td>
</tr>
</table> 

