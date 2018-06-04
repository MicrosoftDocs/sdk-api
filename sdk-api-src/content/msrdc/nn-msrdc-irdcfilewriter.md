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

# IRdcFileWriter interface


## -description


Abstract interface to read from and write to a file.

The RDC application must implement this interface for use with <a href="https://msdn.microsoft.com/6e472ab0-efa4-4edd-8d78-68d5a66cf41c">ISimilarityFileIdTable::CreateTableIndirect</a>. Note that this interface does not include methods to open, close, or flush the file to disk. The application is responsible for properly opening and closing the file represented by an instance of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcFileWriter</b> interface inherits from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>. <b>IRdcFileWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcFileWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/188d43b7-db97-479e-8d4c-e7826d5c3952">DeleteOnClose</a>
</td>
<td align="left" width="63%">
Sets a file to be deleted (or truncated) on close.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71a9a573-a354-47ce-89a0-ebc5acd86159">Truncate</a>
</td>
<td align="left" width="63%">
Truncates a file to zero length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>
</td>
<td align="left" width="63%">
Write bytes to a file starting at a given offset.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

