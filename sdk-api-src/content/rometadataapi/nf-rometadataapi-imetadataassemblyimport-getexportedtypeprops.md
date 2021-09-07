---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetExportedTypeProps
title: IMetaDataAssemblyImport::GetExportedTypeProps (rometadataapi.h)
description: Gets the set of properties of the exported type with the specified metadata signature.
helpviewer_keywords: ["GetExportedTypeProps","GetExportedTypeProps method [Windows Runtime]","GetExportedTypeProps method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","GetExportedTypeProps method","IMetaDataAssemblyImport.GetExportedTypeProps","IMetaDataAssemblyImport::GetExportedTypeProps","rometadataapi/IMetaDataAssemblyImport::GetExportedTypeProps","winrt.imetadataassemblyimport_getexportedtypeprops"]
old-location: winrt\imetadataassemblyimport_getexportedtypeprops.htm
tech.root: WinRT
ms.assetid: bbdd4f9c-f070-463e-91af-4a7c6c6a45d2
ms.date: 12/05/2018
ms.keywords: GetExportedTypeProps, GetExportedTypeProps method [Windows Runtime], GetExportedTypeProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetExportedTypeProps method, IMetaDataAssemblyImport.GetExportedTypeProps, IMetaDataAssemblyImport::GetExportedTypeProps, rometadataapi/IMetaDataAssemblyImport::GetExportedTypeProps, winrt.imetadataassemblyimport_getexportedtypeprops
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
 - IMetaDataAssemblyImport::GetExportedTypeProps
 - rometadataapi/IMetaDataAssemblyImport::GetExportedTypeProps
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
 - IMetaDataAssemblyImport.GetExportedTypeProps
---

# IMetaDataAssemblyImport::GetExportedTypeProps


## -description

Gets the set of properties of the exported type with the specified metadata signature.

## -parameters

### -param mdct [in]

An <b>mdExportedType</b> metadata token that represents the exported type.

### -param szName [out]

The name of the exported type.

### -param cchName [in]

The size, in wide characters, of <i>szName</i>.

### -param pchName [out]

The number of wide characters actually returned in <i>szName</i>.

### -param ptkImplementation [out]

 An <b>mdFile</b>, <b>mdAssemblyRef</b>, or <b>mdExportedType</b> metadata token that contains or allows access to the properties of the exported type.

### -param ptkTypeDef [out]

A pointer to an <b>mdTypeDef</b> token that represents a type in the file.

### -param pdwExportedTypeFlags [out]

A pointer to the flags that describe the metadata applied to the exported type. The flags value can be one or more <a href="/dotnet/framework/unmanaged-api/metadata/cortypeattr-enumeration">CorTypeAttr</a> values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>