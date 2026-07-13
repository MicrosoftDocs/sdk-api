---
UID: NS:dxcapi.IDxcBlobUtf16
tech.root: direct3dhlsl
title: IDxcBlobUtf16
ms.date: 04/05/2023
targetos: Windows
description: TBD
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
req.typenames: 
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
 - IDxcBlobUtf16
f1_keywords:
 - IDxcBlobUtf16
 - dxcapi/IDxcBlobUtf16
dev_langs:
 - c++
helpviewer_keywords:
 - IDxcBlobUtf16
---

## -description

A blob containing a null-terminated wide string, and using the native UTF-16 wide character encoding of Windows. **IDxcBlobUtf16** is a legacy alias for **IDxcBlobWide**. This interface is used to return output name strings in DXC. Other string output blobs (such as errors/warnings, preprocessed HLSL, or other text) are returned using encodings based on the `-encoding` option passed to the compiler. The methods of **IDxcBlobUtf16** guarantee null-terminated text, and native wide character encoding.

## -remarks

## -see-also
