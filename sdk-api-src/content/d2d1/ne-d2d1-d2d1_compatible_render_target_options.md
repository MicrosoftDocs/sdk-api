---
UID: NE:d2d1.D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
title: D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS (d2d1.h)
description: Specifies additional features supportable by a compatible render target when it is created. This enumeration allows a bitwise combination of its member values.
helpviewer_keywords: ["D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS","D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS enumeration [Direct2D]","D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE","D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE","d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS","d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE","d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE","direct2d.D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS"]
old-location: direct2d\D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS.htm
tech.root: Direct2D
ms.assetid: c20bf016-2304-4bd3-88ad-42d81e69c302
ms.date: 12/05/2018
ms.keywords: D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS, D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS enumeration [Direct2D], D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE, D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE, d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS, d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE, d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE, direct2d.D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
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
req.typenames: D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
 - d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
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
 - D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
---

# D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS enumeration


## -description

Specifies additional features supportable by a compatible render target when it is created. 
    This enumeration allows a bitwise combination of its member values.

## -enum-fields

### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE:0x00000000

The render target supports no additional features.

### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE:0x00000001

The render target supports interoperability with the Windows Graphics Device Interface  (GDI).

### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_FORCE_DWORD:0xffffffff

## -remarks

Use this enumeration when creating a compatible render target with the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(constd2d1_size_f_constd2d1_size_u_constd2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)">CreateCompatibleRenderTarget</a> method. For more information about compatible render targets, see the <a href="/windows/win32/Direct2D/render-targets-overview">Render Targets Overview</a>. 

The <b>D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE</b> option may only be requested if the parent render target was created with <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage">D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE</a> (for most render targets) or <b>D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE</b> (for render targets created by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(constd2d1_size_f_constd2d1_size_u_constd2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)">CreateCompatibleRenderTarget</a> method).

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(constd2d1_size_f_constd2d1_size_u_constd2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)">CreateCompatibleRenderTarget</a>



<a href="/windows/win32/Direct2D/render-targets-overview">Render Targets Overview</a>

