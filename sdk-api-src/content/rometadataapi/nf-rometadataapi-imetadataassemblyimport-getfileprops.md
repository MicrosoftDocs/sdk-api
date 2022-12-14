---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetFileProps
title: IMetaDataAssemblyImport::GetFileProps (rometadataapi.h)
description: Gets the properties of the file with the specified metadata signature.
helpviewer_keywords: ["GetFileProps","GetFileProps method [Windows Runtime]","GetFileProps method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","GetFileProps method","IMetaDataAssemblyImport.GetFileProps","IMetaDataAssemblyImport::GetFileProps","rometadataapi/IMetaDataAssemblyImport::GetFileProps","winrt.imetadataassemblyimport_getfileprops"]
old-location: winrt\imetadataassemblyimport_getfileprops.htm
tech.root: WinRT
ms.assetid: 28c884de-3b3c-48cd-9f6f-b2d56005de13
ms.date: 12/05/2018
ms.keywords: GetFileProps, GetFileProps method [Windows Runtime], GetFileProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetFileProps method, IMetaDataAssemblyImport.GetFileProps, IMetaDataAssemblyImport::GetFileProps, rometadataapi/IMetaDataAssemblyImport::GetFileProps, winrt.imetadataassemblyimport_getfileprops
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
 - IMetaDataAssemblyImport::GetFileProps
 - rometadataapi/IMetaDataAssemblyImport::GetFileProps
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
 - IMetaDataAssemblyImport.GetFileProps
---

# IMetaDataAssemblyImport::GetFileProps


## -description

Gets the properties of the file with the specified metadata signature.

## -parameters

### -param mdf [in]

The <b>mdFile</b> metadata token that represents the file for which to get the properties.

### -param szName [out]

The simple name of the file.

### -param cchName [in]

The size, in wide chars, of <i>szName</i>.

### -param pchName [out]

The number of wide chars actually returned in <i>szName</i>.

### -param ppbHashValue [out]

A pointer to the hash value. This is the hash, using the SHA-1 algorithm, of the file.

### -param pcbHashValue [out]

The number of wide chars in the returned hash value.

### -param pdwFileFlags [out]

A pointer to the flags that describe the metadata applied to a file. The flags value is a combination of one or more <a href="/dotnet/framework/unmanaged-api/metadata/corfileflags-enumeration">CorFileFlags</a> values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>