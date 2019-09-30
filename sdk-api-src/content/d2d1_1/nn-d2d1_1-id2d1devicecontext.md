---
UID: NN:d2d1_1.ID2D1DeviceContext
title: ID2D1DeviceContext (d2d1_1.h)
author: windows-sdk-content
description: Represents a set of state and command buffers that are used to render to a target.
old-location: direct2d\id2d1devicecontext.htm
tech.root: Direct2D
ms.assetid: a54dd628-c2a2-4b04-9ced-7749a395f187
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext, ID2D1DeviceContext interface [Direct2D], ID2D1DeviceContext interface [Direct2D],described, d2d1_1/ID2D1DeviceContext, direct2d.id2d1devicecontext
ms.topic: interface
f1_keywords: 
 - "d2d1_1/ID2D1DeviceContext"
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DeviceContext interface


## -description


Represents a set of state and command buffers that are used to render to a target.

The device context can render to a target bitmap or a command list.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>. <b>ID2D1DeviceContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-createbitmap-overload">CreateBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)">DrawBitmap</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> APIs. In addition, color context information can be passed to the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-createbitmapbrush2">CreateBitmapBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates a bitmap brush, the input image is a Direct2D bitmap object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-createbitmapfromdxgisurface">CreateBitmapFromDxgiSurface</a>
</td>
<td align="left" width="63%">Overloaded.  Creates a bitmap from a DXGI surface that can be set as a target surface or have additional color context information specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-createbitmapfromwicbitmap-overload">CreateBitmapFromWicBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates a Direct2D bitmap by copying a WIC bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createcolorcontext">CreateColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createcolorcontextfromfilename">CreateColorContextFromFilename</a>
</td>
<td align="left" width="63%">
Creates a color context by loading it from the specified filename.  The profile bytes are the contents of the file specified by <i>Filename</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createcolorcontextfromwiccolorcontext">CreateColorContextFromWicColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context from an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.  The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">D2D1ColorContext</a> space of the resulting context varies, see Remarks for more info.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createcommandlist">CreateCommandList</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">CreateEffect</a>
</td>
<td align="left" width="63%">
Creates an effect for the specified class ID. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">CreateGradientStopCollection</a>
</td>
<td align="left" width="63%">
Creates a gradient stop collection, enabling the gradient to contain color channels with values outside of [0,1] and also enabling rendering to a high-color render target with interpolation in sRGB space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-createimagebrush-overload">CreateImageBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an image brush. The input image can be any type of image, including a bitmap, effect, or a command list.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-drawbitmap-overload">DrawBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Draws a bitmap to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-drawgdimetafile-overload">DrawGdiMetafile</a>
</td>
<td align="left" width="63%">Overloaded. Draw a metafile to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
Draws a series of glyphs to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-drawimage-overload">DrawImage</a>
</td>
<td align="left" width="63%">Overloaded. Draws an image to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1devicecontext-fillopacitymask-overload">FillOpacityMask</a>
</td>
<td align="left" width="63%">Overloaded. Fill using the alpha channel of the supplied opacity mask bitmap. The brush opacity will be modulated by the mask. The render target antialiasing mode must be set to aliased.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Gets the device associated with a device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-geteffectinvalidrectanglecount">GetEffectInvalidRectangleCount</a>
</td>
<td align="left" width="63%">
Gets the number of invalid output rectangles that have accumulated on the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-geteffectinvalidrectangles">GetEffectInvalidRectangles</a>
</td>
<td align="left" width="63%">
Gets the invalid rectangles that have accumulated since the last time the effect was drawn and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> was then called on the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-geteffectrequiredinputrectangles">GetEffectRequiredInputRectangles</a>
</td>
<td align="left" width="63%">
Returns the input rectangles that are required to be supplied by the caller to produce the given output rectangle. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getglyphrunworldbounds">GetGlyphRunWorldBounds</a>
</td>
<td align="left" width="63%">
    Gets the world-space bounds in DIPs of the glyph run using the device
    context DPI. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getimagelocalbounds">GetImageLocalBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of an image without the world transform of the context applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getimageworldbounds">GetImageWorldBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of an image with the world transform of the context applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getprimitiveblend">GetPrimitiveBlend</a>
</td>
<td align="left" width="63%">
Returns the currently set primitive blend used by the device context.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getrenderingcontrols">GetRenderingControls</a>
</td>
<td align="left" width="63%">
Gets the rendering controls that have been applied to the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-gettarget">GetTarget</a>
</td>
<td align="left" width="63%">
Gets the target currently associated with the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getunitmode">GetUnitMode</a>
</td>
<td align="left" width="63%">
Gets the mode that  is being used to interpret values by the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-invalidateeffectinputrectangle">InvalidateEffectInputRectangle</a>
</td>
<td align="left" width="63%">
This indicates that a portion of an effect's input is invalid. This method can
     be called many times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported">IsBufferPrecisionSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the buffer precision is supported by the underlying Direct3D <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">device.</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported">IsDxgiFormatSupported</a>
</td>
<td align="left" width="63%">
 Indicates whether the format is supported by the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1__id2d1layer)">PushLayer</a>
</td>
<td align="left" width="63%">
Push a layer onto the clip and layer stack of the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setprimitiveblend">SetPrimitiveBlend</a>
</td>
<td align="left" width="63%">
Changes the primitive blend mode that is used for all rendering operations in the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls_)">SetRenderingControls</a>
</td>
<td align="left" width="63%">
Sets the rendering controls for the given device context. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget">SetTarget</a>
</td>
<td align="left" width="63%">
The bitmap or command list to which the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device context will now render.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode">SetUnitMode</a>
</td>
<td align="left" width="63%">
Sets what units will be used to interpret values passed into the device context.

</td>
</tr>
</table> 


## -remarks



 Any resource created from a device context can be shared with any other resource created from a device context when both contexts are created on the same device. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext">D2D1CreateDeviceContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/devices-and-device-contexts">Devices and Device Contexts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext">ID2D1Device::CreateDeviceContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

