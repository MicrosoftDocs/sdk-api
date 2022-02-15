---
UID: NF:rometadataapi.IMetaDataImport.EnumTypeRefs
title: IMetaDataImport::EnumTypeRefs (rometadataapi.h)
description: Enumerates TypeRef tokens defined in the current metadata scope.
helpviewer_keywords: ["EnumTypeRefs","EnumTypeRefs method [Windows Runtime]","EnumTypeRefs method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumTypeRefs method","IMetaDataImport.EnumTypeRefs","IMetaDataImport::EnumTypeRefs","rometadataapi/IMetaDataImport::EnumTypeRefs","winrt.imetadataimport_enumtyperefs"]
old-location: winrt\imetadataimport_enumtyperefs.htm
tech.root: WinRT
ms.assetid: 8d77548d-dfba-4be1-b19d-41b21ab3a112
ms.date: 12/05/2018
ms.keywords: EnumTypeRefs, EnumTypeRefs method [Windows Runtime], EnumTypeRefs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumTypeRefs method, IMetaDataImport.EnumTypeRefs, IMetaDataImport::EnumTypeRefs, rometadataapi/IMetaDataImport::EnumTypeRefs, winrt.imetadataimport_enumtyperefs
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
 - IMetaDataImport::EnumTypeRefs
 - rometadataapi/IMetaDataImport::EnumTypeRefs
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
 - IMetaDataImport.EnumTypeRefs
---

# IMetaDataImport::EnumTypeRefs


## -description

Enumerates TypeRef tokens defined in the current metadata scope.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.

### -param rgTypeRefs [out]

The array used to store the TypeRef tokens.

### -param cMax [in]

The maximum size of the <i>rgTypeRefs</i> array.

### -param pcTypeRefs [out, retval]

A pointer to the number of TypeRef tokens returned in <i>rgTypeRefs</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumTypeRefs </b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTypeRefs</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>