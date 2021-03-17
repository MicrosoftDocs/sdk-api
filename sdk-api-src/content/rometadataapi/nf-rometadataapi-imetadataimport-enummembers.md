---
UID: NF:rometadataapi.IMetaDataImport.EnumMembers
title: IMetaDataImport::EnumMembers (rometadataapi.h)
description: Enumerates MemberDef tokens representing members of the specified type.
helpviewer_keywords: ["EnumMembers","EnumMembers method [Windows Runtime]","EnumMembers method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumMembers method","IMetaDataImport.EnumMembers","IMetaDataImport::EnumMembers","rometadataapi/IMetaDataImport::EnumMembers","winrt.imetadataimport_enummembers"]
old-location: winrt\imetadataimport_enummembers.htm
tech.root: WinRT
ms.assetid: cb1e90fe-e5c8-4f6d-b38a-ae7f46cb34e9
ms.date: 12/05/2018
ms.keywords: EnumMembers, EnumMembers method [Windows Runtime], EnumMembers method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMembers method, IMetaDataImport.EnumMembers, IMetaDataImport::EnumMembers, rometadataapi/IMetaDataImport::EnumMembers, winrt.imetadataimport_enummembers
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
 - IMetaDataImport::EnumMembers
 - rometadataapi/IMetaDataImport::EnumMembers
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
 - IMetaDataImport.EnumMembers
---

# IMetaDataImport::EnumMembers


## -description

Enumerates MemberDef tokens representing members of the specified type.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tkTypeDef [in]

A TypeDef token representing the type whose members are to be enumerated.

### -param rgMembers [out]

The array used to hold the MemberDef tokens.

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
<td><b>EnumMembers</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MemberRef tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -remarks

When enumerating collections of members for a class, <b>EnumMembers</b> returns only members defined directly on the class. It does not return any members that the class inherits, even if the class provides an implementation for those inherited members. To enumerate inherited members, the caller must explicitly walk the inheritance chain. Note that the rules for the inheritance chain may vary depending on the language or compiler that emitted the original metadata.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>