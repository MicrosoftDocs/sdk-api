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

# IWMOutputMediaProps interface


## -description



The <b>IWMOutputMediaProps</b> interface is used to retrieve the properties of an output stream.

An <b>IWMOutputMediaProps</b> object is created by a call to <a href="https://msdn.microsoft.com/e73d13b9-3fca-4de1-b89d-5cacc6311cd3">IWMReader::GetOutputFormat</a> or <a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">IWMReader::GetOutputProps</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMOutputMediaProps</b> interface inherits from <a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>. <b>IWMOutputMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMOutputMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93367398-07aa-4c14-85c8-e3a904bd4564">GetConnectionName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the connection to be used for output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65251316-c98f-46a3-a0cf-164531ef0b46">GetStreamGroupName</a>
</td>
<td align="left" width="63%">
Returns an empty string.

</td>
</tr>
</table> 

For information on which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/96fa7c66-59a0-4eb3-ace4-a827b139f978">Output Media Properties Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps</a>



<a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">IWMReader::SetOutputProps</a>



<a href="https://msdn.microsoft.com/87d16641-3d28-4bad-962b-8ec808cd7877">IWMReaderTypeNegotiation::TryOutputProps</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

