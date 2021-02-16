---
UID: NF:rometadataapi.IMetaDataImport.EnumTypeSpecs
title: IMetaDataImport::EnumTypeSpecs (rometadataapi.h)
description: Enumerates TypeSpec tokens defined in the current metadata scope.
helpviewer_keywords: ["EnumTypeSpecs","EnumTypeSpecs method [Windows Runtime]","EnumTypeSpecs method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumTypeSpecs method","IMetaDataImport.EnumTypeSpecs","IMetaDataImport::EnumTypeSpecs","rometadataapi/IMetaDataImport::EnumTypeSpecs","winrt.imetadataimport_enumtypespecs"]
old-location: winrt\imetadataimport_enumtypespecs.htm
tech.root: WinRT
ms.assetid: 81b3b750-b9bd-42f1-b49d-134a10493ae5
ms.date: 12/05/2018
ms.keywords: EnumTypeSpecs, EnumTypeSpecs method [Windows Runtime], EnumTypeSpecs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumTypeSpecs method, IMetaDataImport.EnumTypeSpecs, IMetaDataImport::EnumTypeSpecs, rometadataapi/IMetaDataImport::EnumTypeSpecs, winrt.imetadataimport_enumtypespecs
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
 - IMetaDataImport::EnumTypeSpecs
 - rometadataapi/IMetaDataImport::EnumTypeSpecs
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
 - IMetaDataImport.EnumTypeSpecs
---

# IMetaDataImport::EnumTypeSpecs


## -description

Enumerates TypeSpec tokens defined in the current metadata scope.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This value must be NULL for the first call of this method.

### -param rgTypeSpecs [out]

The array used to store the TypeSpec tokens.

### -param cMax [in]

The maximum size of the <i>rgTypeSpecs</i> array.

### -param pcTypeSpecs [out]

The number of TypeSpec tokens returned in <i>rgTypeSpecs</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumTypeSpecs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTypeSpecs</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>