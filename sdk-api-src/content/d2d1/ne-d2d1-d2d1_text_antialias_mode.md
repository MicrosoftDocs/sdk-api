---
UID: NE:d2d1.D2D1_TEXT_ANTIALIAS_MODE
title: D2D1_TEXT_ANTIALIAS_MODE (d2d1.h)
description: Describes the antialiasing mode used for drawing text.
helpviewer_keywords: ["D2D1_TEXT_ANTIALIAS_MODE","D2D1_TEXT_ANTIALIAS_MODE enumeration [Direct2D]","D2D1_TEXT_ANTIALIAS_MODE_ALIASED","D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE","D2D1_TEXT_ANTIALIAS_MODE_DEFAULT","D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE","d2d1/D2D1_TEXT_ANTIALIAS_MODE","d2d1/D2D1_TEXT_ANTIALIAS_MODE_ALIASED","d2d1/D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE","d2d1/D2D1_TEXT_ANTIALIAS_MODE_DEFAULT","d2d1/D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE","direct2d.D2D1_TEXT_ANTIALIAS_MODE"]
old-location: direct2d\D2D1_TEXT_ANTIALIAS_MODE.htm
tech.root: Direct2D
ms.assetid: d2c829d7-9892-4cbb-9993-12bb7d77fc25
ms.date: 12/05/2018
ms.keywords: D2D1_TEXT_ANTIALIAS_MODE, D2D1_TEXT_ANTIALIAS_MODE enumeration [Direct2D], D2D1_TEXT_ANTIALIAS_MODE_ALIASED, D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE, D2D1_TEXT_ANTIALIAS_MODE_DEFAULT, D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE, d2d1/D2D1_TEXT_ANTIALIAS_MODE, d2d1/D2D1_TEXT_ANTIALIAS_MODE_ALIASED, d2d1/D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE, d2d1/D2D1_TEXT_ANTIALIAS_MODE_DEFAULT, d2d1/D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE, direct2d.D2D1_TEXT_ANTIALIAS_MODE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_TEXT_ANTIALIAS_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TEXT_ANTIALIAS_MODE
 - d2d1/D2D1_TEXT_ANTIALIAS_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_TEXT_ANTIALIAS_MODE
---

# D2D1_TEXT_ANTIALIAS_MODE enumeration


## -description

Describes the antialiasing mode used for drawing text.

## -enum-fields

### -field D2D1_TEXT_ANTIALIAS_MODE_DEFAULT:0

Use the system default. See Remarks.

### -field D2D1_TEXT_ANTIALIAS_MODE_CLEARTYPE:1

Use ClearType antialiasing.

### -field D2D1_TEXT_ANTIALIAS_MODE_GRAYSCALE:2

Use grayscale antialiasing.

### -field D2D1_TEXT_ANTIALIAS_MODE_ALIASED:3

Do not use antialiasing.

### -field D2D1_TEXT_ANTIALIAS_MODE_FORCE_DWORD:0xffffffff

## -remarks

This enumeration is used with the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a> of an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a> to specify how text and glyphs are antialiased.

 By default, Direct2D renders text in ClearType mode. Factors that 

can downgrade the default quality to grayscale or aliased:

<ul>
<li>If the <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a> value  is <b>DWRITE_RENDERING_MODE_ALIASED </b>, then the 

default text antialiasing mode is aliased.  To change the DirectWrite rendering mode of an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>, use the  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams">ID2D1RenderTarget::SetTextRenderingParams</a> method. </li>
<li>If the <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a> value is <b>DWRITE_RENDERING_MODE_OUTLINE</b>, then the default text 

antialiasing mode is grayscale.</li>
<li>If the render target has an alpha channel and is not set to <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_IGNORE</a>, then 

the default text antialiasing mode is grayscale.</li>
<li>If <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">ID2D1RenderTarget::PushLayer</a>  is called without <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_layer_options">D2D1_LAYER_OPTIONS_INITIALIZE_FOR_CLEARTYPE</a> 

(and the corresponding <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> has not  been called yet), then the default text 

antialiasing mode is grayscale.</li>
</ul>

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">ID2D1RenderTarget::SetTextAntialiasMode</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams">ID2D1RenderTarget::SetTextRenderingParams</a>

