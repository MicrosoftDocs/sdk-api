---
UID: NF:dxcapi.IDxcUtils.MoveToBlob
tech.root: 
title: IDxcUdirect3dhlsltils::MoveToBlob
ms.date: 04/05/2023
targetos: Windows
description: Create a blob, taking ownership of the memory allocated by the supplied allocator.
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
 - IDxcUtils::MoveToBlob
f1_keywords:
 - IDxcUtils::MoveToBlob
 - dxcapi/IDxcUtils::MoveToBlob
dev_langs:
 - c++
helpviewer_keywords:
 - MoveToBlob
---

## -description

Create a blob, taking ownership of the memory that's allocated by the supplied allocator.

Use this method in preference to [IDxcLibrary::CreateBlobWithEncodingOnMalloc](./nf-dxcapi-idxclibrary-createblobwithencodingonmalloc.md).

## -parameters

### -param pData

A pointer to a buffer containing the contents of the new blob.

### -param pIMalloc

The memory allocator to use.

### -param size

The size of the *pData* buffer, in bytes.

### -param codePage

The code page to use if the blob contains text. For binary or ANSI code page, use **DXC_CP_ACP**.

### -param pBlobEncoding

The address of the pointer that receives a pointer to the newly-created blob.

## -returns

## -remarks

## -see-also
