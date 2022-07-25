---
UID: NF:rometadataapi.IMetaDataImport2.GetGenericParamConstraintProps
title: IMetaDataImport2::GetGenericParamConstraintProps (rometadataapi.h)
description: Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.
helpviewer_keywords: ["GetGenericParamConstraintProps","GetGenericParamConstraintProps method [Windows Runtime]","GetGenericParamConstraintProps method [Windows Runtime]","IMetaDataImport2 interface","IMetaDataImport2 interface [Windows Runtime]","GetGenericParamConstraintProps method","IMetaDataImport2.GetGenericParamConstraintProps","IMetaDataImport2::GetGenericParamConstraintProps","rometadataapi/IMetaDataImport2::GetGenericParamConstraintProps","winrt.imetadataimport2_getgenericparamconstraintprops"]
old-location: winrt\imetadataimport2_getgenericparamconstraintprops.htm
tech.root: WinRT
ms.assetid: 307b4ab5-733d-4340-a400-3a13039099b0
ms.date: 12/05/2018
ms.keywords: GetGenericParamConstraintProps, GetGenericParamConstraintProps method [Windows Runtime], GetGenericParamConstraintProps method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetGenericParamConstraintProps method, IMetaDataImport2.GetGenericParamConstraintProps, IMetaDataImport2::GetGenericParamConstraintProps, rometadataapi/IMetaDataImport2::GetGenericParamConstraintProps, winrt.imetadataimport2_getgenericparamconstraintprops
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
 - IMetaDataImport2::GetGenericParamConstraintProps
 - rometadataapi/IMetaDataImport2::GetGenericParamConstraintProps
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
 - IMetaDataImport2.GetGenericParamConstraintProps
---

# IMetaDataImport2::GetGenericParamConstraintProps


## -description

Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.

## -parameters

### -param gpc [in]

The token to the generic parameter constraint for which to return the metadata.

### -param ptGenericParam [out]

A pointer to the token that represents the generic parameter that is constrained.

### -param ptkConstraintType [out]

A pointer to a <b>TypeDef</b>, <b>TypeRef</b>, or <b>TypeSpec</b> token that represents a constraint on ptGenericParam.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport2">IMetaDataImport2</a>