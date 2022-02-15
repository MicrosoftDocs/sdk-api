---
UID: NE:dcommon.D2D1_ALPHA_MODE
title: D2D1_ALPHA_MODE (dcommon.h)
description: Specifies how the alpha value of a bitmap or render target should be treated.
helpviewer_keywords: ["D2D1_ALPHA_MODE","D2D1_ALPHA_MODE enumeration [Direct2D]","D2D1_ALPHA_MODE_IGNORE","D2D1_ALPHA_MODE_PREMULTIPLIED","D2D1_ALPHA_MODE_STRAIGHT","D2D1_ALPHA_MODE_UNKNOWN","dcommon/D2D1_ALPHA_MODE","dcommon/D2D1_ALPHA_MODE_IGNORE","dcommon/D2D1_ALPHA_MODE_PREMULTIPLIED","dcommon/D2D1_ALPHA_MODE_STRAIGHT","dcommon/D2D1_ALPHA_MODE_UNKNOWN","direct2d.D2D1_ALPHA_MODE"]
old-location: direct2d\D2D1_ALPHA_MODE.htm
tech.root: Direct2D
ms.assetid: f1b1e735-2e89-4dc1-9fee-dfb4626ef453
ms.date: 12/05/2018
ms.keywords: D2D1_ALPHA_MODE, D2D1_ALPHA_MODE enumeration [Direct2D], D2D1_ALPHA_MODE_IGNORE, D2D1_ALPHA_MODE_PREMULTIPLIED, D2D1_ALPHA_MODE_STRAIGHT, D2D1_ALPHA_MODE_UNKNOWN, dcommon/D2D1_ALPHA_MODE, dcommon/D2D1_ALPHA_MODE_IGNORE, dcommon/D2D1_ALPHA_MODE_PREMULTIPLIED, dcommon/D2D1_ALPHA_MODE_STRAIGHT, dcommon/D2D1_ALPHA_MODE_UNKNOWN, direct2d.D2D1_ALPHA_MODE
req.header: dcommon.h
req.include-header: D2d1.h
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
req.typenames: D2D1_ALPHA_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_ALPHA_MODE
 - dcommon/D2D1_ALPHA_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcommon.h
api_name:
 - D2D1_ALPHA_MODE
---

# D2D1_ALPHA_MODE enumeration


## -description

Specifies how the alpha value of a bitmap or render target should be treated.

## -enum-fields

### -field D2D1_ALPHA_MODE_UNKNOWN:0

The alpha value might not be meaningful.

### -field D2D1_ALPHA_MODE_PREMULTIPLIED:1

The alpha value has been premultiplied. Each color is first scaled by the alpha value. The alpha value itself is the same in both straight and premultiplied alpha. Typically, no color channel value is greater than the alpha channel value.  If a color channel value in a premultiplied format is greater than the alpha channel, the standard source-over blending math results in an additive blend.

### -field D2D1_ALPHA_MODE_STRAIGHT:2

The alpha value has not been premultiplied. The alpha channel indicates the transparency of the color.

### -field D2D1_ALPHA_MODE_IGNORE:3

The alpha value is ignored.

### -field D2D1_ALPHA_MODE_FORCE_DWORD:0xffffffff

## -remarks

The <b>D2D1_ALPHA_MODE</b> enumeration is used with the <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a> enumeration to specify the alpha mode of a render target or bitmap. Different render targets and bitmaps support different alpha modes. For a list, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

<h3><a id="The_Differences_Between_Straight_and_Premultiplied_Alpha"></a><a id="the_differences_between_straight_and_premultiplied_alpha"></a><a id="THE_DIFFERENCES_BETWEEN_STRAIGHT_AND_PREMULTIPLIED_ALPHA"></a>The Differences Between Straight and Premultiplied Alpha</h3>
When describing an RGBA color using straight alpha, the alpha value of the color is stored in the alpha channel. For example, to describe a red color that is 60% opaque, you'd use the following values: (255, 0, 0, 255 * 0.6) = (255, 0, 0, 153). The 255 value indicates full red, and 153 (which is 60 percent of 255) indicates that the color should have an opacity of 60 percent.

When describing an RGBA color using premultiplied alpha, each color is multiplied by the alpha value: (255 * 0.6, 0 * 0.6, 0 * 0.6, 255 * 0.6) = (153, 0, 0, 153).  

Regardless of the alpha mode of the render target, <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a> values are always interpreted as straight alpha.  For example, when specifying the color of an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a> for use with a bitmap that uses the premultiplied alpha mode, you'd specify the color just as you would if the bitmap used straight alpha. When you paint with the brush, Direct2D translates the color to the destination format for you.

<h3><a id="Alpha_Mode_for_Render_Targets"></a><a id="alpha_mode_for_render_targets"></a><a id="ALPHA_MODE_FOR_RENDER_TARGETS"></a>Alpha Mode for Render Targets</h3>
Regardless of the alpha mode setting, a render target's contents support transparency. For example, if you draw a partially transparent red rectangle with a render target with an alpha mode of <b>D2D1_ALPHA_MODE_IGNORE</b>, the rectangle will appear pink (if the background is white), as you might expect.

If you draw a partially transparent red rectangle when the alpha mode is [CreateCompatibleRenderTarget](../d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget).md) method) to create a bitmap that supports transparency. 

<h3><a id="ClearType_and_Alpha_Modes"></a><a id="cleartype_and_alpha_modes"></a><a id="CLEARTYPE_AND_ALPHA_MODES"></a>ClearType and Alpha Modes</h3>
If you specify an alpha mode other than <b>D2D1_ALPHA_MODE_IGNORE</b> for a render target, the text antialiasing mode automatically changes from <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE CLEARTYPE</a>  to <b>D2D1_TEXT_ANTIALIAS_MODE GRAYSCALE</b>. (When you specify an alpha mode of <b>D2D1_ALPHA_MODE_UNKNOWN</b>, Direct2D sets the alpha for you depending on the type of render target. For a list of what the <b>D2D1_ALPHA_MODE_UNKNOWN</b> setting resolves to for each render target, see the <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a> overview.) 

You can use the <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a> method to change the text antialias mode  back to <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode">D2D1_TEXT_ANTIALIAS_MODE CLEARTYPE</a>, but rendering ClearType text to a transparent surface can create unpredictable results. If you want to render ClearType text to a transparent render target, we recommend that you use one of the following two techniques. 

<ul>
<li>Use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)">PushAxisAlignedClip</a> method to clip the render target to the area where the text will be rendered,    then call the <a href="/windows/desktop/Direct2D/id2d1rendertarget-clear">Clear</a> method and specify an opaque color, then render your text.</li>
<li>Use <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)">DrawRectangle</a> to draw an opaque rectangle behind the area where the text will be rendered.</li>
</ul>

## -see-also

<a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>
