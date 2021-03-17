---
UID: NF:rometadataapi.IMetaDataImport.EnumMembersWithName
title: IMetaDataImport::EnumMembersWithName (rometadataapi.h)
description: Enumerates MemberDef tokens representing members of the specified type with the specified name.
helpviewer_keywords: ["EnumMembersWithName","EnumMembersWithName method [Windows Runtime]","EnumMembersWithName method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumMembersWithName method","IMetaDataImport.EnumMembersWithName","IMetaDataImport::EnumMembersWithName","rometadataapi/IMetaDataImport::EnumMembersWithName","winrt.imetadataimport_enummemberswithname"]
old-location: winrt\imetadataimport_enummemberswithname.htm
tech.root: WinRT
ms.assetid: cfb72609-7db5-4780-aeeb-b3effa37665a
ms.date: 12/05/2018
ms.keywords: EnumMembersWithName, EnumMembersWithName method [Windows Runtime], EnumMembersWithName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMembersWithName method, IMetaDataImport.EnumMembersWithName, IMetaDataImport::EnumMembersWithName, rometadataapi/IMetaDataImport::EnumMembersWithName, winrt.imetadataimport_enummemberswithname
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMetaDataImport::EnumMembersWithName
 - rometadataapi/IMetaDataImport::EnumMembersWithName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataImport.EnumMembersWithName
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

This method enumerates fields and methods, but not properties or events. Unlike <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummembers">EnumMembers</a>, <b>EnumMembersWithName</b> discards all field and member tokens that do not have the specified name.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>