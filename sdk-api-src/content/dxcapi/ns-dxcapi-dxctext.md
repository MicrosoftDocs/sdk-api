---
UID: NS:dxcapi.DxcBuffer
tech.root: direct3dhlsl
title: DxcText
ms.date: 04/05/2023
targetos: Windows
description: Structure for supplying bytes or text input to Dxc APIs.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DxcText
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - DxcBuffer
 - DxcText
f1_keywords:
 - DxcBuffer
 - dxcapi/DxcBuffer
 - DxcText
 - dxcapi/DxcText
dev_langs:
 - c++
helpviewer_keywords:
 - DxcBuffer
---

## -description

Structure for supplying bytes or text input to Dxc APIs.

## -struct-fields

### -field Ptr

A pointer to the start of the buffer.

### -field Size

The size of the buffer, in bytes.

### -field Encoding

The encoding of the buffer. Use Encoding == 0 for non-text bytes, ANSI text, or unknown with byte-order mark (BOM).

## -remarks

## -see-also
