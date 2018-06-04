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

# CItemIDFactory class


## -description


Exposes methods for interacting with Shell data sources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CItemIDFactory</b> class inherits from <a href="https://msdn.microsoft.com/16db01f3-4167-43f0-9ef7-34eec906e199">IDelegateFolder</a>. <b>CItemIDFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>CItemIDFactory</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2129F4F3-A989-4CE2-ABFF-FE83DD78D4CE">CreateItemID</a>
</td>
<td align="left" width="63%">
Creates an ItemID from the supplied data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E3E2233D-F424-4BF9-AAC4-4DC2FB75E214">GetDataFromIDList</a>
</td>
<td align="left" width="63%">
Gets a read only pointer to the client provided structure in the first ItemID in the IDList.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D0BE2A9A-5832-4C0E-BFB6-96EB467C3D9D">GetPropertyFromIDList</a>
</td>
<td align="left" width="63%">Overloaded. Returns a property from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> within the IDList.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A3F0F28-C9E1-4F2E-9A02-C6A48BF3C204">GetPropertyStorage</a>
</td>
<td align="left" width="63%">
Gets  a read only pointer to the serialized property storage that is used for storing metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50E8F4F9-1E7B-4314-9AFB-1CA0795776FE">GetPropertyStorageFromIDList</a>
</td>
<td align="left" width="63%">
create an instance of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> based on the serialized property storage associated with the first ItemID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/269DFCDF-A5F7-4367-8B08-3A5015BB04FE">IsDelegateFolder</a>
</td>
<td align="left" width="63%">
Gets a Boolean value specifying whether the factory is a delegate folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3E2BAAD9-5C16-4ECF-BADB-16B355439BA5">SetItemAlloc</a>
</td>
<td align="left" width="63%">
Provides the <b>CItemIDFactory</b> an <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface used to allocate and free item IDs.

</td>
</tr>
</table> 


## -remarks



it is recomended that all data sources use this as it manages an important issue of security when  dealing with IDList parsing.




## -see-also




<a href="https://msdn.microsoft.com/16db01f3-4167-43f0-9ef7-34eec906e199">IDelegateFolder</a>
 

 

