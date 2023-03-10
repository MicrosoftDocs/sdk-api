---
UID: NF:rometadataapi.IMetaDataImport2.GetGenericParamProps
title: IMetaDataImport2::GetGenericParamProps (rometadataapi.h)
description: Gets the metadata associated with the generic parameter represented by the specified token.
helpviewer_keywords: ["GetGenericParamProps","GetGenericParamProps method [Windows Runtime]","GetGenericParamProps method [Windows Runtime]","IMetaDataImport2 interface","IMetaDataImport2 interface [Windows Runtime]","GetGenericParamProps method","IMetaDataImport2.GetGenericParamProps","IMetaDataImport2::GetGenericParamProps","rometadataapi/IMetaDataImport2::GetGenericParamProps","winrt.imetadataimport2_getgenericparamprops"]
old-location: winrt\imetadataimport2_getgenericparamprops.htm
tech.root: WinRT
ms.assetid: 3967e82c-64e3-4d05-b10a-e4e86f9f60ab
ms.date: 12/05/2018
ms.keywords: GetGenericParamProps, GetGenericParamProps method [Windows Runtime], GetGenericParamProps method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetGenericParamProps method, IMetaDataImport2.GetGenericParamProps, IMetaDataImport2::GetGenericParamProps, rometadataapi/IMetaDataImport2::GetGenericParamProps, winrt.imetadataimport2_getgenericparamprops
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
 - IMetaDataImport2::GetGenericParamProps
 - rometadataapi/IMetaDataImport2::GetGenericParamProps
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
 - IMetaDataImport2.GetGenericParamProps
---

# IMetaDataImport2::GetGenericParamProps


## -description

Gets the metadata associated with the generic parameter represented by the specified token.

## -parameters

### -param gp [in]

The token that represents the generic parameter for which to return metadata.

### -param pulParamSeq [out]

The ordinal position of the Type parameter in the parent constructor or method.

### -param pdwParamFlags [out]

 A value of the <a href="/dotnet/framework/unmanaged-api/metadata/corgenericparamattr-enumeration">CorGenericParamAttr</a> enumeration that describes the Type for the generic parameter.

### -param ptOwner [out]

A  <b>TypeDef</b> or <b>MethodDef</b> token that represents the owner of the parameter.

### -param reserved [out]

Reserved for future extensibility.

### -param wzname [out]

The name of the generic parameter.

### -param cchName [in]

The size of the <i>wzName</i> buffer.

### -param pchName [out]

The returned size of the name, in wide characters.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport2">IMetaDataImport2</a>