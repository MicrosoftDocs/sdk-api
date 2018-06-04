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

# IMetaDataImport::EnumMembersWithName


## -description


Enumerates MemberDef tokens representing members of the specified type with the specified name.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator.


### -param tkTypeDef [in]

A TypeDef token representing the type with members to enumerate.


### -param szName [in]

The member name that limits the scope of the enumerator.


### -param rgMembers [out]

The array used to store the MemberDef tokens.


### -param cMax [in]

The maximum size of the <i>rgMembers</i> array.


### -param pcTokens [out]

The actual number of MemberDef tokens returned in <i>rgMembers</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMembersWithName</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MemberRef tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -remarks



This method enumerates fields and methods, but not properties or events. Unlike <a href="https://msdn.microsoft.com/cb1e90fe-e5c8-4f6d-b38a-ae7f46cb34e9">EnumMembers</a>, <b>EnumMembersWithName</b> discards all field and member tokens that do not have the specified name.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

