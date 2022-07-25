---
UID: NF:rometadataapi.IMetaDataImport.FindTypeDefByName
title: IMetaDataImport::FindTypeDefByName (rometadataapi.h)
description: Gets a pointer to the TypeDef metadata token for the Type with the specified name.
helpviewer_keywords: ["FindTypeDefByName","FindTypeDefByName method [Windows Runtime]","FindTypeDefByName method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","FindTypeDefByName method","IMetaDataImport.FindTypeDefByName","IMetaDataImport::FindTypeDefByName","rometadataapi/IMetaDataImport::FindTypeDefByName","winrt.imetadataimport_findtypedefbyname"]
old-location: winrt\imetadataimport_findtypedefbyname.htm
tech.root: WinRT
ms.assetid: dd4dd7d9-dfdf-4095-881b-c730ebfb083c
ms.date: 12/05/2018
ms.keywords: FindTypeDefByName, FindTypeDefByName method [Windows Runtime], FindTypeDefByName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],FindTypeDefByName method, IMetaDataImport.FindTypeDefByName, IMetaDataImport::FindTypeDefByName, rometadataapi/IMetaDataImport::FindTypeDefByName, winrt.imetadataimport_findtypedefbyname
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
 - IMetaDataImport::FindTypeDefByName
 - rometadataapi/IMetaDataImport::FindTypeDefByName
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
 - IMetaDataImport.FindTypeDefByName
---

# IMetaDataImport::FindTypeDefByName


## -description

Gets a pointer to the TypeDef metadata token for the Type with the specified name.

## -parameters

### -param szTypeDef [in]

The name of the type for which to get the TypeDef token.

### -param tkEnclosingClass [in]

A TypeDef or TypeRef token representing the enclosing class. If the type to find is not a nested class, set this value to NULL.

### -param ptkTypeDef [out, retval]

A pointer to the matching TypeDef token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>