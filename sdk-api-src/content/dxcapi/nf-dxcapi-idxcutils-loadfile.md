---
UID: NF:dxcapi.IDxcUtils.LoadFile
tech.root: direct3dhlsl
title: IDxcUtils::LoadFile
ms.date: 04/05/2023
targetos: Windows
description: Create a blob with data loaded from a file.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - IDxcUtils::LoadFile
f1_keywords:
 - IDxcUtils::LoadFile
 - dxcapi/IDxcUtils::LoadFile
dev_langs:
 - c++
helpviewer_keywords:
 - LoadFile
---

## -description

Create a blob with data loaded from a file. The new blob and its contents are allocated with the current allocator.

Use this method in preference to [IDxcLibrary::CreateBlobFromFile](./nf-dxcapi-idxclibrary-createblobfromfile.md).

## -parameters

### -param pFileName

The name of the file to load from.

### -param pCodePage

An optional code page to use if the blob contains text. For binary data, pass **NULL**.

### -param pBlobEncoding

The address of the pointer that receives a pointer to the newly-created blob.

## -returns

## -remarks

## -see-also
