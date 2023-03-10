---
UID: NE:d2d1_1.D2D1_MAP_OPTIONS
title: D2D1_MAP_OPTIONS (d2d1_1.h)
description: Specifies how the memory to be mapped from the corresponding ID2D1Bitmap1 should be treated.
helpviewer_keywords: ["D2D1_MAP_OPTIONS","D2D1_MAP_OPTIONS enumeration [Direct2D]","D2D1_MAP_OPTIONS_DISCARD","D2D1_MAP_OPTIONS_READ","D2D1_MAP_OPTIONS_WRITE","d2d1_1/D2D1_MAP_OPTIONS","d2d1_1/D2D1_MAP_OPTIONS_DISCARD","d2d1_1/D2D1_MAP_OPTIONS_READ","d2d1_1/D2D1_MAP_OPTIONS_WRITE","direct2d.__d2d1_map_options"]
old-location: direct2d\__d2d1_map_options.htm
tech.root: Direct2D
ms.assetid: 8706c3e3-eb29-4760-bdfd-f19afc6f2bf7
ms.date: 12/05/2018
ms.keywords: D2D1_MAP_OPTIONS, D2D1_MAP_OPTIONS enumeration [Direct2D], D2D1_MAP_OPTIONS_DISCARD, D2D1_MAP_OPTIONS_READ, D2D1_MAP_OPTIONS_WRITE, d2d1_1/D2D1_MAP_OPTIONS, d2d1_1/D2D1_MAP_OPTIONS_DISCARD, d2d1_1/D2D1_MAP_OPTIONS_READ, d2d1_1/D2D1_MAP_OPTIONS_WRITE, direct2d.__d2d1_map_options
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_MAP_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_MAP_OPTIONS
 - d2d1_1/D2D1_MAP_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_MAP_OPTIONS
---

# D2D1_MAP_OPTIONS enumeration


## -description

Specifies how the memory to be mapped from the corresponding <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a> should be treated.

## -enum-fields

### -field D2D1_MAP_OPTIONS_NONE:0

### -field D2D1_MAP_OPTIONS_READ:1

Allow CPU Read access.

### -field D2D1_MAP_OPTIONS_WRITE:2

Allow CPU Write access.

### -field D2D1_MAP_OPTIONS_DISCARD:4

Discard the previous contents of the resource when it is mapped.

### -field D2D1_MAP_OPTIONS_FORCE_DWORD:0xffffffff

## -remarks

The <b>D2D1_MAP_OPTIONS_READ</b> option can be used only if the bitmap was created with the <b>D2D1_BITMAP_OPTIONS_CPU_READ</b> flag.

These flags will be not be able to be used on bitmaps created by the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>. However, the ID2D1SourceTransform will receive bitmaps for which these flags are valid.

<b>D2D1_MAP_OPTIONS_DISCARD</b> can only be used with <b>D2D1_MAP_OPTIONS_WRITE</b>.  Both of these options are only available through the effect author API, not through the Direct2D rendering API.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map">ID2D1Bitmap1::Map</a>
