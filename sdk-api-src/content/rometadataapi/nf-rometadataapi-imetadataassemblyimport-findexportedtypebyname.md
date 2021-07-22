---
UID: NF:rometadataapi.IMetaDataAssemblyImport.FindExportedTypeByName
title: IMetaDataAssemblyImport::FindExportedTypeByName (rometadataapi.h)
description: Gets a pointer to an exported type, given its name and enclosing type.
helpviewer_keywords: ["FindExportedTypeByName","FindExportedTypeByName method [Windows Runtime]","FindExportedTypeByName method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","FindExportedTypeByName method","IMetaDataAssemblyImport.FindExportedTypeByName","IMetaDataAssemblyImport::FindExportedTypeByName","rometadataapi/IMetaDataAssemblyImport::FindExportedTypeByName","winrt.imetadataassemblyimport_findexportedtypebyname"]
old-location: winrt\imetadataassemblyimport_findexportedtypebyname.htm
tech.root: WinRT
ms.assetid: 2b19b41c-fd1b-4284-8455-2b0d69907c99
ms.date: 12/05/2018
ms.keywords: FindExportedTypeByName, FindExportedTypeByName method [Windows Runtime], FindExportedTypeByName method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],FindExportedTypeByName method, IMetaDataAssemblyImport.FindExportedTypeByName, IMetaDataAssemblyImport::FindExportedTypeByName, rometadataapi/IMetaDataAssemblyImport::FindExportedTypeByName, winrt.imetadataassemblyimport_findexportedtypebyname
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
 - IMetaDataAssemblyImport::FindExportedTypeByName
 - rometadataapi/IMetaDataAssemblyImport::FindExportedTypeByName
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
 - IMetaDataAssemblyImport.FindExportedTypeByName
---

# IMetaDataAssemblyImport::FindExportedTypeByName


## -description

Gets a pointer to an exported type, given its name and enclosing type.

## -parameters

### -param szName [in]

The name of the exported type.

### -param mdtExportedType [in]

The metadata token for the enclosing class of the exported type. This value is <b>mdExportedTypeNil</b> if the requested exported type is not a nested type.

### -param ptkExportedType [out]

A pointer to the <b>mdExportedType</b> token that represents the exported type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method uses the standard rules employed by the common language runtime for resolving references.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>