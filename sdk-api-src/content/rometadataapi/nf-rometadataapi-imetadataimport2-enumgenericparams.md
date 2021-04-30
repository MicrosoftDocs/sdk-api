---
UID: NF:rometadataapi.IMetaDataImport2.EnumGenericParams
title: IMetaDataImport2::EnumGenericParams (rometadataapi.h)
description: Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.
helpviewer_keywords: ["EnumGenericParams","EnumGenericParams method [Windows Runtime]","EnumGenericParams method [Windows Runtime]","IMetaDataImport2 interface","IMetaDataImport2 interface [Windows Runtime]","EnumGenericParams method","IMetaDataImport2.EnumGenericParams","IMetaDataImport2::EnumGenericParams","rometadataapi/IMetaDataImport2::EnumGenericParams","winrt.imetadataimport2_enumgenericparams"]
old-location: winrt\imetadataimport2_enumgenericparams.htm
tech.root: WinRT
ms.assetid: 7ad0d834-7b77-4c90-b28f-fc9e54e9deb7
ms.date: 12/05/2018
ms.keywords: EnumGenericParams, EnumGenericParams method [Windows Runtime], EnumGenericParams method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],EnumGenericParams method, IMetaDataImport2.EnumGenericParams, IMetaDataImport2::EnumGenericParams, rometadataapi/IMetaDataImport2::EnumGenericParams, winrt.imetadataimport2_enumgenericparams
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
 - IMetaDataImport2::EnumGenericParams
 - rometadataapi/IMetaDataImport2::EnumGenericParams
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
 - IMetaDataImport2.EnumGenericParams
---

# IMetaDataImport2::EnumGenericParams


## -description

Gets an enumerator for an array of generic parameter tokens associated with the specified TypeDef or MethodDef token.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator.

### -param tk [in]

The <b>TypeDef</b> or <b>MethodDef</b> token whose generic parameters are to be enumerated.

### -param rGenericParams [out]

The array of generic parameters to enumerate.

### -param cMax [in]

The requested maximum number of tokens to place in <i>rGenericParams</i>.

### -param pcGenericParams [out]

The returned number of tokens placed in <i>rGenericParams</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumGenericParams</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td><i>phEnum</i> has no member elements. In this case, <i>pcGenericParams</i> is set to 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport2">IMetaDataImport2</a>