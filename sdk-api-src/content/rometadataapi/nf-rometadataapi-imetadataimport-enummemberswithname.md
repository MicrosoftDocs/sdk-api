---
UID: NF:rometadataapi.IMetaDataImport.EnumMembersWithName
title: IMetaDataImport::EnumMembersWithName
author: windows-sdk-content
description: Enumerates MemberDef tokens representing members of the specified type with the specified name.
old-location: winrt\imetadataimport_enummemberswithname.htm
old-project: WinRT
ms.assetid: cfb72609-7db5-4780-aeeb-b3effa37665a
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: EnumMembersWithName, EnumMembersWithName method [Windows Runtime], EnumMembersWithName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMembersWithName method, IMetaDataImport.EnumMembersWithName, IMetaDataImport::EnumMembersWithName, rometadataapi/IMetaDataImport::EnumMembersWithName, winrt.imetadataimport_enummemberswithname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.EnumMembersWithName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

