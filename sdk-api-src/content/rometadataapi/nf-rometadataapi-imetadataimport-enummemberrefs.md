---
UID: NF:rometadataapi.IMetaDataImport.EnumMemberRefs
title: IMetaDataImport::EnumMemberRefs (rometadataapi.h)
description: Enumerates MemberRef tokens representing members of the specified type.
helpviewer_keywords: ["EnumMemberRefs","EnumMemberRefs method [Windows Runtime]","EnumMemberRefs method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumMemberRefs method","IMetaDataImport.EnumMemberRefs","IMetaDataImport::EnumMemberRefs","rometadataapi/IMetaDataImport::EnumMemberRefs","winrt.imetadataimport_enummemberrefs"]
old-location: winrt\imetadataimport_enummemberrefs.htm
tech.root: WinRT
ms.assetid: 900777d4-14fc-4d64-a01c-395f5fafe5e4
ms.date: 12/05/2018
ms.keywords: EnumMemberRefs, EnumMemberRefs method [Windows Runtime], EnumMemberRefs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMemberRefs method, IMetaDataImport.EnumMemberRefs, IMetaDataImport::EnumMemberRefs, rometadataapi/IMetaDataImport::EnumMemberRefs, winrt.imetadataimport_enummemberrefs
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
 - IMetaDataImport::EnumMemberRefs
 - rometadataapi/IMetaDataImport::EnumMemberRefs
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
 - IMetaDataImport.EnumMemberRefs
---

# IMetaDataImport::EnumMemberRefs


## -description

Enumerates MemberRef tokens representing members of the specified type.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tkParent [in]

A TypeDef, TypeRef, MethodDef, or ModuleRef token for the type whose members are to be enumerated.

### -param rgMemberRefs [out]

The array used to store MemberRef tokens.

### -param cMax [in]

The maximum size of the <i>rgMemberRefs</i> array.

### -param pcTokens [out]

The actual number of MemberRef tokens returned in <i>rgMemberRefs</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMemberRefs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no MemberRef tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>