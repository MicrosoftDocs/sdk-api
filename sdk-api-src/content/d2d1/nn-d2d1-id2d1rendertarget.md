---
UID: NN:d2d1.ID2D1RenderTarget
title: ID2D1RenderTarget (d2d1.h)
description: Represents an object that can receive drawing commands. Interfaces that inherit from ID2D1RenderTarget render the drawing commands they receive in different ways.helpviewer_keywords: ["ID2D1RenderTarget","ID2D1RenderTarget interface [Direct2D]","ID2D1RenderTarget interface [Direct2D]","described","d2d1/ID2D1RenderTarget","direct2d.ID2D1RenderTarget"]
old-location: direct2d\ID2D1RenderTarget.htm
tech.root: Direct2D
ms.assetid: 40629be9-5840-4bde-b369-56bbfd791775
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget, ID2D1RenderTarget interface [Direct2D], ID2D1RenderTarget interface [Direct2D],described, d2d1/ID2D1RenderTarget, direct2d.ID2D1RenderTarget
f1_keywords:
- d2d1/ID2D1RenderTarget
dev_langs:
- c++
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
req.lib: D2d1.lib
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
- ID2D1RenderTarget
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget interface


## -description


Represents an object that can receive drawing commands. Interfaces that inherit from <b>ID2D1RenderTarget</b> render the drawing commands they receive in different ways.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1RenderTarget</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1RenderTarget</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -members

The <b>ID2D1RenderTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates drawing on this render target. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-clear">Clear</a>
</td>
<td align="left" width="63%">Overloaded. Clears the drawing area to the specified color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-createbitmap">CreateBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates a Direct2D bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-createbitmapbrush">CreateBitmapBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> from the specified bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-createbitmapfromwicbitmap">CreateBitmapFromWicBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC)  bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(constd2d1_size_f_constd2d1_size_u_constd2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)">CreateCompatibleRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new  bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-creategradientstopcollection">CreateGradientStopCollection</a>
</td>
<td align="left" width="63%">Overloaded.      Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> from the specified array of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-createlayer">CreateLayer</a>
</td>
<td align="left" width="63%">Overloaded. Creates a layer resource that can be used with this render target and its compatible render targets. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-createlineargradientbrush">CreateLinearGradientBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> object for painting areas with a linear gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createmesh">CreateMesh</a>
</td>
<td align="left" width="63%">
Create a mesh that uses triangles to describe a shape.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-createradialgradientbrush">CreateRadialGradientBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a> object that can be used to paint areas with a radial gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap">CreateSharedBitmap</a>
</td>
<td align="left" width="63%">
Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> whose data is shared with another resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-createsolidcolorbrush">CreateSolidColorBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush">ID2D1SolidColorBrush</a> that can be used to paint areas with a solid color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-drawbitmap">DrawBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Draws the specified <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-drawellipse">DrawEllipse</a>
</td>
<td align="left" width="63%">Overloaded. Draws the outline of an ellipse with the specified dimensions and stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry">DrawGeometry</a>
</td>
<td align="left" width="63%">
Draws the outline of the specified geometry using the specified stroke style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
Draws the specified glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline">DrawLine</a>
</td>
<td align="left" width="63%">
Draws a line between the specified points using the specified stroke style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-drawrectangle">DrawRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Draws the outline of a rectangle that has the specified dimensions and stroke style.
    

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-drawroundedrectangle">DrawRoundedRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Draws the outline of the specified rounded rectangle using the specified stroke style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-drawtext">DrawText</a>
</td>
<td align="left" width="63%">Overloaded. Draws the specified text using the format information provided by an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">DrawTextLayout</a>
</td>
<td align="left" width="63%">
Draws the formatted text described by the specified <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a>
</td>
<td align="left" width="63%">
Ends drawing operations  on the render target and indicates the current error state and associated tags. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-fillellipse">FillEllipse</a>
</td>
<td align="left" width="63%">Overloaded. Paints the interior of the specified ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry">FillGeometry</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillmesh">FillMesh</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified mesh.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-fillopacitymask">FillOpacityMask</a>
</td>
<td align="left" width="63%">Overloaded. Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-fillrectangle">FillRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Paints the interior of the specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-fillroundedrectangle">FillRoundedRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Paints the interior of the specified rounded rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a>
</td>
<td align="left" width="63%">
Executes all pending drawing commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getantialiasmode">GetAntialiasMode</a>
</td>
<td align="left" width="63%">
Retrieves the current antialiasing mode for nontext drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getdpi">GetDpi</a>
</td>
<td align="left" width="63%">
Return the render target's dots per inch (DPI).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getmaximumbitmapsize">GetMaximumBitmapSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size, in device-dependent units (pixels), of  any one bitmap dimension supported by the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format and alpha mode of the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize">GetPixelSize</a>
</td>
<td align="left" width="63%">
Returns the size of the render target in device pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Returns the size of the render target in device-independent pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags">GetTags</a>
</td>
<td align="left" width="63%">
Gets the label for subsequent drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettextantialiasmode">GetTextAntialiasMode</a>
</td>
<td align="left" width="63%">
Gets the current antialiasing mode for text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettextrenderingparams">GetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Retrieves the render target's current text rendering options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform">GetTransform</a>
</td>
<td align="left" width="63%">
Gets the current transform of the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties_)">IsSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the render target supports the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip">PopAxisAlignedClip</a>
</td>
<td align="left" width="63%">
Removes the last axis-aligned clip from the render target. After this method is called, the clip is no longer applied to subsequent drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a>
</td>
<td align="left" width="63%">
Stops redirecting drawing operations to the layer that is specified by the last <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a> call. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-pushaxisalignedclip">PushAxisAlignedClip</a>
</td>
<td align="left" width="63%">Overloaded. Specifies a rectangle to which all subsequent drawing operations are clipped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-pushlayer">PushLayer</a>
</td>
<td align="left" width="63%">Overloaded. Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> is called. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-restoredrawingstate">RestoreDrawingState</a>
</td>
<td align="left" width="63%">
Sets the render target's drawing state to that of the specified <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-savedrawingstate">SaveDrawingState</a>
</td>
<td align="left" width="63%">
Saves the current drawing state to the specified <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode">SetAntialiasMode</a>
</td>
<td align="left" width="63%">
Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setdpi">SetDpi</a>
</td>
<td align="left" width="63%">
Sets the dots per inch (DPI) of the render target. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags">SetTags</a>
</td>
<td align="left" width="63%">
Specifies a label for subsequent drawing operations.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a>
</td>
<td align="left" width="63%">
Specifies the antialiasing mode to use for subsequent text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams">SetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Specifies text rendering options to be applied to all subsequent text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/Direct2D/id2d1rendertarget-settransform">SetTransform</a>
</td>
<td align="left" width="63%">Overloaded. Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space.

</td>
</tr>
</table> 


## -remarks



Your application should create render targets once and hold onto them for the life of the application or until the render target's  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created). 




## -see-also




<a href="/windows/win32/Direct2D/the-direct2d-api">Direct2D API Overview</a>



<a href="/windows/win32/Direct2D/getting-started-with-direct2d-nav">Getting Started</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>
 

 

