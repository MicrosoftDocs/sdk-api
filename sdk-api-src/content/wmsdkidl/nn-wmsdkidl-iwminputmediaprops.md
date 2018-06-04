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

# IWMInputMediaProps interface


## -description



The <b>IWMInputMediaProps</b> interface is used to retrieve the properties of digital media that will be passed to the writer.

An input media properties object is created by a call to either the <a href="https://msdn.microsoft.com/2889a1a7-3111-4c13-b15a-659f519c22f6">IWMWriter::GetInputProps</a> or <a href="https://msdn.microsoft.com/c058de81-a29a-4bcd-a819-3cdef11cae9f">IWMWriter::GetInputFormat</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMInputMediaProps</b> interface inherits from <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>. <b>IWMInputMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMInputMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efb8b26b-c04f-4253-85a7-13456e1599bb">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the connection name specified in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/795cd065-62f1-4346-b2ff-f77ec4306d64">GetGroupName</a>
</td>
<td align="left" width="63%">
Not implemented in this release. Returns an empty string.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/e7aa6c99-b6b3-4e5b-869d-3387f70dad87">Input Media Properties Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps Interface</a>



<a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/c058de81-a29a-4bcd-a819-3cdef11cae9f">IWMWriter::GetInputFormat</a>



<a href="https://msdn.microsoft.com/2889a1a7-3111-4c13-b15a-659f519c22f6">IWMWriter::GetInputProps</a>



<a href="https://msdn.microsoft.com/15084a4d-06e8-4f74-9697-ced794d2cdae">IWMWriter::SetInputProps</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

