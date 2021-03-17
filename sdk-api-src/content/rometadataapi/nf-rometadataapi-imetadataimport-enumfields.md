---
UID: NF:rometadataapi.IMetaDataImport.EnumFields
title: IMetaDataImport::EnumFields (rometadataapi.h)
description: Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.
helpviewer_keywords: ["EnumFields","EnumFields method [Windows Runtime]","EnumFields method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumFields method","IMetaDataImport.EnumFields","IMetaDataImport::EnumFields","rometadataapi/IMetaDataImport::EnumFields","winrt.imetadataimport_enumfields"]
old-location: winrt\imetadataimport_enumfields.htm
tech.root: WinRT
ms.assetid: c9f8f389-fdb2-404b-a24e-cf2cf119bf55
ms.date: 12/05/2018
ms.keywords: EnumFields, EnumFields method [Windows Runtime], EnumFields method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumFields method, IMetaDataImport.EnumFields, IMetaDataImport::EnumFields, rometadataapi/IMetaDataImport::EnumFields, winrt.imetadataimport_enumfields
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
 - IMetaDataImport::EnumFields
 - rometadataapi/IMetaDataImport::EnumFields
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
 - IMetaDataImport.EnumFields
---

# IMetaDataImport::EnumFields


## -description

Enumerates FieldDef tokens for the type referenced by the specified TypeDef token.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tkTypeDef [in]

The TypeDef token of the class whose fields are to be enumerated.

### -param rgFields [out]

The list of FieldDef tokens.

### -param cMax [in]

The maximum size of the <i>rgFields</i> array.

### -param pcTokens [out]

The actual number of FieldDef tokens returned in <i>rgFields</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumFields</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no fields to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>