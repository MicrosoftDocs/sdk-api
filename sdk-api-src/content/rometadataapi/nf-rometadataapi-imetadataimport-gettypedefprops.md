---
UID: NF:rometadataapi.IMetaDataImport.GetTypeDefProps
title: IMetaDataImport::GetTypeDefProps (rometadataapi.h)
description: Returns metadata information for the Type represented by the specified TypeDef token.
helpviewer_keywords: ["GetTypeDefProps","GetTypeDefProps method [Windows Runtime]","GetTypeDefProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetTypeDefProps method","IMetaDataImport.GetTypeDefProps","IMetaDataImport::GetTypeDefProps","rometadataapi/IMetaDataImport::GetTypeDefProps","winrt.imetadataimport_gettypedefprops"]
old-location: winrt\imetadataimport_gettypedefprops.htm
tech.root: WinRT
ms.assetid: 447937af-5edb-4e5e-89a1-13d1a733b3f7
ms.date: 12/05/2018
ms.keywords: GetTypeDefProps, GetTypeDefProps method [Windows Runtime], GetTypeDefProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetTypeDefProps method, IMetaDataImport.GetTypeDefProps, IMetaDataImport::GetTypeDefProps, rometadataapi/IMetaDataImport::GetTypeDefProps, winrt.imetadataimport_gettypedefprops
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
 - IMetaDataImport::GetTypeDefProps
 - rometadataapi/IMetaDataImport::GetTypeDefProps
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
 - IMetaDataImport.GetTypeDefProps
---

# IMetaDataImport::GetTypeDefProps


## -description

Returns metadata information for the Type represented by the specified TypeDef token.

## -parameters

### -param tkTypeDef [in]

The TypeDef token that represents the type to return metadata for.

### -param szTypeDef [out]

A buffer containing the type name.

### -param cchTypeDef [in]

The size in wide characters of <i>szTypeDef</i>.

### -param pchTypeDef [out]

The number of wide characters returned in <i>szTypeDef</i>.

### -param pdwTypeDefFlags [out]

A pointer to any flags that modify the type definition. This value is a bitmask from the <a href="/dotnet/framework/unmanaged-api/metadata/cortypeattr-enumeration">CorTypeAttr</a> enumeration.

### -param ptkExtends [out]

A TypeDef or TypeRef metadata token that represents the base type of the requested type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>