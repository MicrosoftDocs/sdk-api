---
UID: NL:shidfact.CItemIDFactory
title: CItemIDFactory
author: windows-sdk-content
description: Exposes methods for interacting with Shell data sources.
old-location: shell\citemidfactory.htm
old-project: shell
ms.assetid: 8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CItemIDFactory, CItemIDFactory class [Windows Shell], CItemIDFactory class [Windows Shell],described, shell.citemidfactory, shidfact/CItemIDFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shidfact.h
api_name:
-	CItemIDFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
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
 

 

