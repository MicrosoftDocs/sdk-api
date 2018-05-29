---
UID: NE:dcommon.D2D1_ALPHA_MODE
title: D2D1_ALPHA_MODE
author: windows-sdk-content
description: Specifies how the alpha value of a bitmap or render target should be treated.
old-location: direct2d\D2D1_ALPHA_MODE.htm
old-project: Direct2D
ms.assetid: f1b1e735-2e89-4dc1-9fee-dfb4626ef453
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1_ALPHA_MODE, D2D1_ALPHA_MODE enumeration [Direct2D], D2D1_ALPHA_MODE_IGNORE, D2D1_ALPHA_MODE_PREMULTIPLIED, D2D1_ALPHA_MODE_STRAIGHT, D2D1_ALPHA_MODE_UNKNOWN, dcommon/D2D1_ALPHA_MODE, dcommon/D2D1_ALPHA_MODE_IGNORE, dcommon/D2D1_ALPHA_MODE_PREMULTIPLIED, dcommon/D2D1_ALPHA_MODE_STRAIGHT, dcommon/D2D1_ALPHA_MODE_UNKNOWN, direct2d.D2D1_ALPHA_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dcommon.h
req.include-header: D2d1.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_ALPHA_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dcommon.h
api_name:
-	D2D1_ALPHA_MODE
product: Windows
targetos: Windows
req.lib: Dciman32.lib
req.dll: Dciman32.dll
req.irql: 
---

# D2D1_ALPHA_MODE enumeration


## -description


Specifies how the alpha value of a bitmap or render target should be treated.


## -enum-fields




### -field D2D1_ALPHA_MODE_UNKNOWN

The alpha value might not be meaningful.


### -field D2D1_ALPHA_MODE_PREMULTIPLIED

The alpha value has been premultiplied. Each color is first scaled by the alpha value. The alpha value itself is the same in both straight and premultiplied alpha. Typically, no color channel value is greater than the alpha channel value.  If a color channel value in a premultiplied format is greater than the alpha channel, the standard source-over blending math results in an additive blend.


### -field D2D1_ALPHA_MODE_STRAIGHT

The alpha value has not been premultiplied. The alpha channel indicates the transparency of the color. 


### -field D2D1_ALPHA_MODE_IGNORE

The alpha value is ignored.


### -field D2D1_ALPHA_MODE_FORCE_DWORD




## -remarks



The <b>D2D1_ALPHA_MODE</b> enumeration is used with the <a href="https://msdn.microsoft.com/e95afd9c-5793-4cb7-bcb8-aae4d28b6532">D2D1_PIXEL_FORMAT</a> enumeration to specify the alpha mode of a render target or bitmap. Different render targets and bitmaps support different alpha modes. For a list, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.

<h3><a id="The_Differences_Between_Straight_and_Premultiplied_Alpha"></a><a id="the_differences_between_straight_and_premultiplied_alpha"></a><a id="THE_DIFFERENCES_BETWEEN_STRAIGHT_AND_PREMULTIPLIED_ALPHA"></a>The Differences Between Straight and Premultiplied Alpha</h3>
When describing an RGBA color using straight alpha, the alpha value of the color is stored in the alpha channel. For example, to describe a red color that is 60% opaque, you'd use the following values: (255, 0, 0, 255 * 0.6) = (255, 0, 0, 153). The 255 value indicates full red, and 153 (which is 60 percent of 255) indicates that the color should have an opacity of 60 percent.

When describing an RGBA color using premultiplied alpha, each color is multiplied by the alpha value: (255 * 0.6, 0 * 0.6, 0 * 0.6, 255 * 0.6) = (153, 0, 0, 153).  

Regardless of the alpha mode of the render target, <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a> values are always interpreted as straight alpha.  For example, when specifying the color of an <a href="https://msdn.microsoft.com/a15c2696-3122-461e-806e-2195a50a3e92">ID2D1SolidColorBrush</a> for use with a bitmap that uses the premultiplied alpha mode, you'd specify the color just as you would if the bitmap used straight alpha. When you paint with the brush, Direct2D translates the color to the destination format for you.

<h3><a id="Alpha_Mode_for_Render_Targets"></a><a id="alpha_mode_for_render_targets"></a><a id="ALPHA_MODE_FOR_RENDER_TARGETS"></a>Alpha Mode for Render Targets</h3>
Regardless of the alpha mode setting, a render target's contents support transparency. For example, if you draw a partially transparent red rectangle with a render target with an alpha mode of <b>D2D1_ALPHA_MODE_IGNORE</b>, the rectangle will appear pink (if the background is white), as you might expect.

If you draw a partially transparent red rectangle when the alpha mode is <b>D2D1_ALPHA_MODE_PREMULTIPLIED</b>, the rectangle will appear pink (assuming the background is white) and you can see through it to whatever is behind the render target. This is useful when using a <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a> to render to a transparent window or when using an compatible render target (a render targeted created by the <a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a> method) to create a bitmap that supports transparency. 

<h3><a id="ClearType_and_Alpha_Modes"></a><a id="cleartype_and_alpha_modes"></a><a id="CLEARTYPE_AND_ALPHA_MODES"></a>ClearType and Alpha Modes</h3>
If you specify an alpha mode other than <b>D2D1_ALPHA_MODE_IGNORE</b> for a render target, the text antialiasing mode automatically changes from <a href="https://msdn.microsoft.com/d2c829d7-9892-4cbb-9993-12bb7d77fc25">D2D1_TEXT_ANTIALIAS_MODE CLEARTYPE</a>  to <b>D2D1_TEXT_ANTIALIAS_MODE GRAYSCALE</b>. (When you specify an alpha mode of <b>D2D1_ALPHA_MODE_UNKNOWN</b>, Direct2D sets the alpha for you depending on the type of render target. For a list of what the <b>D2D1_ALPHA_MODE_UNKNOWN</b> setting resolves to for each render target, see the <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a> overview.) 

You can use the <a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a> method to change the text antialias mode  back to <a href="https://msdn.microsoft.com/d2c829d7-9892-4cbb-9993-12bb7d77fc25">D2D1_TEXT_ANTIALIAS_MODE CLEARTYPE</a>, but rendering ClearType text to a transparent surface can create unpredictable results. If you want to render ClearType text to an transparent render target, we recommend that you use one of the following two techniques. 

<ul>
<li>Use the <a href="https://msdn.microsoft.com/8b777425-07b1-4494-889a-0c947fb61315">PushAxisAlignedClip</a> method to clip the render target to the area where the text will be rendered,    then call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a> method and specify an opaque color, then render your text.</li>
<li>Use <a href="https://msdn.microsoft.com/3f8c0754-fa68-4b5b-812f-24d8b544ba6e">DrawRectangle</a> to draw an opaque rectangle behind the area where the text will be rendered.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

