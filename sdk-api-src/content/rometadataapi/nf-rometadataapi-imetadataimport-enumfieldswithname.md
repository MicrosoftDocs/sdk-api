---
UID: NF:rometadataapi.IMetaDataImport.EnumFieldsWithName
title: IMetaDataImport::EnumFieldsWithName (rometadataapi.h)
description: Enumerates FieldDef tokens of the specified type with the specified name.
helpviewer_keywords: ["EnumFieldsWithName","EnumFieldsWithName method [Windows Runtime]","EnumFieldsWithName method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumFieldsWithName method","IMetaDataImport.EnumFieldsWithName","IMetaDataImport::EnumFieldsWithName","rometadataapi/IMetaDataImport::EnumFieldsWithName","winrt.imetadataimport_enumfieldswithname"]
old-location: winrt\imetadataimport_enumfieldswithname.htm
tech.root: WinRT
ms.assetid: 6035f267-778d-4d7d-84eb-1081f33ff619
ms.date: 12/05/2018
ms.keywords: EnumFieldsWithName, EnumFieldsWithName method [Windows Runtime], EnumFieldsWithName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumFieldsWithName method, IMetaDataImport.EnumFieldsWithName, IMetaDataImport::EnumFieldsWithName, rometadataapi/IMetaDataImport::EnumFieldsWithName, winrt.imetadataimport_enumfieldswithname
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
 - IMetaDataImport::EnumFieldsWithName
 - rometadataapi/IMetaDataImport::EnumFieldsWithName
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
 - IMetaDataImport.EnumFieldsWithName
---

# IMetaDataImport::EnumFieldsWithName


## -description

Enumerates FieldDef tokens of the specified type with the specified name.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tkTypeDef [in]

The token of the type whose fields are to be enumerated.

### -param szName [in]

The field name that limits the scope of the enumeration.

### -param rFields [out]

Array used to store the FieldDef tokens.

### -param cMax [in]

The maximum size of the <i>rFields</i> array.

### -param pcTokens [out]

The actual number of FieldDef tokens returned in <i>rFields</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumFieldsWithName</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no fields to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -remarks

Unlike <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enumfields">EnumFields</a>, <b>EnumFieldsWithName</b> discards all field tokens that do not have the specified name.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>