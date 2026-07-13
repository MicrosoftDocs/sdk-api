---
UID: NF:dxcapi.IDxcUtils.CreateBlob
tech.root: direct3dhlsl
title: IDxcUtils::CreateBlob
ms.date: 04/05/2023
targetos: Windows
description: Copy blob contents to memory that's owned by the new blob. New blobs and copied contents are allocated with the current allocator.
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
 - IDxcUtils::CreateBlob
f1_keywords:
 - IDxcUtils::CreateBlob
 - dxcapi/IDxcUtils::CreateBlob
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBlob
---

## -description

Create a blob containing a copy of the existing data. The new blob and its contents are allocated with the current allocator.

Use this method in preference to [IDxcLibrary::CreateBlobWithEncodingOnHeapCopy](./nf-dxcapi-idxclibrary-createblobwithencodingonheapcopy.md).

## -parameters

### -param pData

A pointer to a buffer containing the contents of the new blob.

### -param size

The size of the *pData* buffer, in bytes.

### -param codePage

The code page to use if the blob contains text. For binary or ANSI code page, use **DXC_CP_ACP**.

### -param pBlobEncoding

The address of the pointer that receives a pointer to the newly-created blob.

## -returns

## -remarks

## -see-also
