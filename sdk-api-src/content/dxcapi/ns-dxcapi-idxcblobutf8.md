---
UID: NS:dxcapi.IDxcBlobUtf8
tech.root: direct3dhlsl
title: IDxcBlobUtf8
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
 - IDxcBlobUtf8
f1_keywords:
 - IDxcBlobUtf8
 - dxcapi/IDxcBlobUtf8
dev_langs:
 - c++
helpviewer_keywords:
 - IDxcBlobUtf8
---

## -description

A blob containing a null-terminated string, and using the UTF-8 character encoding. Depending on the `-encoding` option passed to the compiler, this interface is used to return string output blobs (such as errors/warnings, preprocessed HLSL, or other text). The methods of **IDxcBlobUtf8** guarantee null-terminated text, and UTF-8 character encoding. [IDxcBlobUtf16](./ns-dxcapi-idxcblobutf16) is used to return output name strings in DXC.

## -remarks

## -see-also
