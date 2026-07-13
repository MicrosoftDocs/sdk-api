---
UID: NF:dxcapi.IDxcUtils.CreateBlobFromPinned
tech.root: direct3dhlsl
title: IDxcUtils::CreateBlobFromPinned
ms.date: 04/05/2023
targetos: Windows
description: Creates a blob referencing existing memory, with no copy. You must manage the memory lifetime separately.
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
 - IDxcUtils::CreateBlobFromPinned
f1_keywords:
 - IDxcUtils::CreateBlobFromPinned
 - dxcapi/IDxcUtils::CreateBlobFromPinned
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBlobFromPinned
---

## -description

Creates a blob referencing existing memory, with no copy. You must manage the memory lifetime separately.

Use this method in preference to [IDxcLibrary::CreateBlobWithEncodingFromPinned](./nf-dxcapi-idxclibrary-createblobwithencodingfrompinned.md).

## -parameters

### -param pData

Pointer to a buffer containing the contents of the new blob.

### -param size

The size of the pData buffer, in bytes.

### -param codePage

The code page to use if the blob contains text. For binary or ANSI code page, use **DXC_CP_ACP**.

### -param pBlobEncoding

Address of the pointer that receives a pointer to the newly-created blob.

## -returns

## -remarks

## -see-also
