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

# IMultisessionSequential interface


## -description


Use this interface to retrieve information about the previous import session on a sequentially recorded media, if the media contains a previous session. 

The following methods return a collection of <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a> interfaces representing all supported multisession types. <ul>
<li>
<a href="https://msdn.microsoft.com/7bb2d100-629f-4b63-a699-ddce85213e72">IDiscFormat2Data::get_MultisessionInterfaces</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10c0b02e-965e-47ca-95f4-237c21b505ad">IFileSystemImage::get_MultisessionInterfaces</a>
</li>
</ul>The <b>IMultisession::QueryInterface</b> method can be called on each element in the collection to query for the <b>IMultisessionSequential</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultisessionSequential</b> interface inherits from <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>. <b>IMultisessionSequential</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultisessionSequential</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d308a080-8858-4d80-8203-bce9f8d9bed6">get_FreeSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the number of free sectors available on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dd7a321-833a-4fee-8128-675d1b76736c">get_IsFirstDataSession</a>
</td>
<td align="left" width="63%">
Determines if this session is the first data session on the media. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a37aa4d1-0862-463d-acf1-3a85e491ef26">get_LastWrittenAddressOfPreviousSession</a>
</td>
<td align="left" width="63%">
Retrieves the last sector written in the previous session on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52bc2a66-e2ac-473b-8b17-1c2d642a76f8">get_NextWritableAddress</a>
</td>
<td align="left" width="63%">
Retrieves the next writable address on the media, including used sectors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97819e2a-c01b-4820-a200-d9e9c6928f1b">get_StartAddressOfPreviousSession</a>
</td>
<td align="left" width="63%">
Retrieves the first sector written in the previous session on the media.

</td>
</tr>
</table> 


## -remarks



If more than one multi-session interface exist, the application can let <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a> choose a compatible multi-session interface to use  or the application can specify the multi-session interface to use by setting the <a href="https://msdn.microsoft.com/d4eef9de-8b7e-4326-b66f-dddbe2b8a05d">put_InUse</a> property to VARIANT_TRUE.

A file system creator would use the address properties to import the content of the previous session on the disc and to compute the position of the next session it will create. These properties will return the same values as the properties of the same name of the <a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a> interface.

This is a <b>MsftMultisessionSequential</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>
 

 

