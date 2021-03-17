---
UID: NF:rometadataapi.IMetaDataImport2.EnumGenericParamConstraints
title: IMetaDataImport2::EnumGenericParamConstraints (rometadataapi.h)
description: Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.
helpviewer_keywords: ["EnumGenericParamConstraints","EnumGenericParamConstraints method [Windows Runtime]","EnumGenericParamConstraints method [Windows Runtime]","IMetaDataImport2 interface","IMetaDataImport2 interface [Windows Runtime]","EnumGenericParamConstraints method","IMetaDataImport2.EnumGenericParamConstraints","IMetaDataImport2::EnumGenericParamConstraints","rometadataapi/IMetaDataImport2::EnumGenericParamConstraints","winrt.imetadataimport2_enumgenericparamconstraints"]
old-location: winrt\imetadataimport2_enumgenericparamconstraints.htm
tech.root: WinRT
ms.assetid: 5e8ba48d-7c94-4fc6-8def-db296065fdce
ms.date: 12/05/2018
ms.keywords: EnumGenericParamConstraints, EnumGenericParamConstraints method [Windows Runtime], EnumGenericParamConstraints method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],EnumGenericParamConstraints method, IMetaDataImport2.EnumGenericParamConstraints, IMetaDataImport2::EnumGenericParamConstraints, rometadataapi/IMetaDataImport2::EnumGenericParamConstraints, winrt.imetadataimport2_enumgenericparamconstraints
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
 - IMetaDataImport2::EnumGenericParamConstraints
 - rometadataapi/IMetaDataImport2::EnumGenericParamConstraints
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
 - IMetaDataImport2.EnumGenericParamConstraints
---

# IMetaDataImport2::EnumGenericParamConstraints


## -description

Gets an enumerator for an array of generic parameter constraints associated with the generic parameter represented by the specified token.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tk [in]

A token that represents the generic parameter whose constraints are to be enumerated.

### -param rGenericParamConstraints [out]

The array of generic parameter constraints to enumerate.

### -param cMax [in]

The requested maximum number of tokens to place in <i>rGenericParamConstraints</i>.

### -param pcGenericParamConstraints [out]

A pointer to the number of tokens placed in <i>rGenericParamConstraints</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumGenericParamConstraints</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td><i>phEnum</i> has no member elements. In this case, <i>pcGenericParameterConstraints</i> is set to 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport2">IMetaDataImport2</a>