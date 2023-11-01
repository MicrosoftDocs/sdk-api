---
UID: NF:dxcapi.IDxcUtils.CreateBlobFromBlob
tech.root: direct3dhlsl
title: IDxcUtils::CreateBlobFromBlob
ms.date: 04/05/2023
targetos: Windows
description: Create a sub-blob that holds a reference to the outer blob, and points to its memory.
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
 - IDxcUtils::CreateBlobFromBlob
f1_keywords:
 - IDxcUtils::CreateBlobFromBlob
 - dxcapi/IDxcUtils::CreateBlobFromBlob
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBlobFromBlob
---

## -description

Create a sub-blob that holds a reference to the outer blob, and points to its memory.

## -parameters

### -param pBlob

The outer blob.

### -param offset

The offset inside the outer blob.

### -param length

The size, in bytes, of the buffer to reference from the output blob.

### -param ppResult

Address of the pointer that receives a pointer to the newly-created blob.

## -returns

## -remarks

## -see-also
