---
UID: NE:d2d1_1.D2D1_BUFFER_PRECISION
title: D2D1_BUFFER_PRECISION (d2d1_1.h)
description: Represents the bit depth of the imaging pipeline in Direct2D.
helpviewer_keywords: ["D2D1_BUFFER_PRECISION","D2D1_BUFFER_PRECISION enumeration [Direct2D]","D2D1_BUFFER_PRECISION_16BPC_FLOAT","D2D1_BUFFER_PRECISION_16BPC_UNORM","D2D1_BUFFER_PRECISION_32BPC_FLOAT","D2D1_BUFFER_PRECISION_8BPC_UNORM","D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB","D2D1_BUFFER_PRECISION_FORCE_DWORD","D2D1_BUFFER_PRECISION_UNKNOWN","d2d1_1/D2D1_BUFFER_PRECISION","d2d1_1/D2D1_BUFFER_PRECISION_16BPC_FLOAT","d2d1_1/D2D1_BUFFER_PRECISION_16BPC_UNORM","d2d1_1/D2D1_BUFFER_PRECISION_32BPC_FLOAT","d2d1_1/D2D1_BUFFER_PRECISION_8BPC_UNORM","d2d1_1/D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB","d2d1_1/D2D1_BUFFER_PRECISION_FORCE_DWORD","d2d1_1/D2D1_BUFFER_PRECISION_UNKNOWN","direct2d.__d2d1_buffer_precision"]
old-location: direct2d\__d2d1_buffer_precision.htm
tech.root: Direct2D
ms.assetid: a2a4b4fd-685d-4068-b1f5-609e6ab024e2
ms.date: 12/05/2018
ms.keywords: D2D1_BUFFER_PRECISION, D2D1_BUFFER_PRECISION enumeration [Direct2D], D2D1_BUFFER_PRECISION_16BPC_FLOAT, D2D1_BUFFER_PRECISION_16BPC_UNORM, D2D1_BUFFER_PRECISION_32BPC_FLOAT, D2D1_BUFFER_PRECISION_8BPC_UNORM, D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB, D2D1_BUFFER_PRECISION_FORCE_DWORD, D2D1_BUFFER_PRECISION_UNKNOWN, d2d1_1/D2D1_BUFFER_PRECISION, d2d1_1/D2D1_BUFFER_PRECISION_16BPC_FLOAT, d2d1_1/D2D1_BUFFER_PRECISION_16BPC_UNORM, d2d1_1/D2D1_BUFFER_PRECISION_32BPC_FLOAT, d2d1_1/D2D1_BUFFER_PRECISION_8BPC_UNORM, d2d1_1/D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB, d2d1_1/D2D1_BUFFER_PRECISION_FORCE_DWORD, d2d1_1/D2D1_BUFFER_PRECISION_UNKNOWN, direct2d.__d2d1_buffer_precision
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
req.typenames: D2D1_BUFFER_PRECISION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BUFFER_PRECISION
 - d2d1_1/D2D1_BUFFER_PRECISION
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
 - D2D1_BUFFER_PRECISION
---

# D2D1_BUFFER_PRECISION enumeration


## -description

Represents the bit depth of the imaging pipeline in Direct2D.

## -enum-fields

### -field D2D1_BUFFER_PRECISION_UNKNOWN:0

The buffer precision is not specified.

### -field D2D1_BUFFER_PRECISION_8BPC_UNORM:1

Use 8-bit normalized integer per channel.

### -field D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB:2

Use 8-bit normalized integer standard RGB data per channel.

### -field D2D1_BUFFER_PRECISION_16BPC_UNORM:3

Use 16-bit normalized integer per channel.

### -field D2D1_BUFFER_PRECISION_16BPC_FLOAT:4

Use 16-bit floats per channel.

### -field D2D1_BUFFER_PRECISION_32BPC_FLOAT:5

Use 32-bit floats per channel.

### -field D2D1_BUFFER_PRECISION_FORCE_DWORD:0xffffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.

Do not use this value.

## -remarks

<div class="alert"><b>Note</b>   Feature level 9 may or may not support precision types other than 8BPC.
</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_rendering_controls">D2D1_RENDERING_CONTROLS</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getrenderingcontrols">ID2D1DeviceContext::GetRenderingControls</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls_)">ID2D1DeviceContext::SetRenderingControls</a>
