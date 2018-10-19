---
UID: NN:d2d1.ID2D1RenderTarget
title: ID2D1RenderTarget
author: windows-sdk-content
description: Represents an object that can receive drawing commands. Interfaces that inherit from ID2D1RenderTarget render the drawing commands they receive in different ways.
old-location: direct2d\ID2D1RenderTarget.htm
tech.root: direct2d
ms.assetid: 40629be9-5840-4bde-b369-56bbfd791775
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1RenderTarget, ID2D1RenderTarget interface [Direct2D], ID2D1RenderTarget interface [Direct2D],described, d2d1/ID2D1RenderTarget, direct2d.ID2D1RenderTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget interface


## -description


Represents an object that can receive drawing commands. Interfaces that inherit from <b>ID2D1RenderTarget</b> render the drawing commands they receive in different ways.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1RenderTarget</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1RenderTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates drawing on this render target. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bfec923-17fc-479a-a760-9baab2ff3a56">Clear</a>
</td>
<td align="left" width="63%">Overloaded. Clears the drawing area to the specified color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b45d353f-ae33-4110-b7c8-f14661017e0f">CreateBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates a Direct2D bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f6ef07e-4271-4605-aced-f191a0fe65af">CreateBitmapBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> from the specified bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/463fc2f9-8ec6-47e8-8d48-a9015616e656">CreateBitmapFromWicBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC)  bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new  bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">CreateGradientStopCollection</a>
</td>
<td align="left" width="63%">Overloaded.      Creates an <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> from the specified array of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> structures. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7">CreateLayer</a>
</td>
<td align="left" width="63%">Overloaded. Creates a layer resource that can be used with this render target and its compatible render targets. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc07113f-ff93-4b0f-8328-02dd481dccb0">CreateLinearGradientBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/bbb5e36a-d13d-448e-8686-d14ee99b1ccb">ID2D1LinearGradientBrush</a> object for painting areas with a linear gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c0036d8-1f91-4d90-a301-b58bde8da974">CreateMesh</a>
</td>
<td align="left" width="63%">
Create a mesh that uses triangles to describe a shape.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/985a4c1b-d29b-46ed-bc55-6dcd313718a8">CreateRadialGradientBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/21ed2286-e4df-4b77-ba31-e5d5927e16f5">ID2D1RadialGradientBrush</a> object that can be used to paint areas with a radial gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6377dbd-ffd9-458b-9e03-5a832f095818">CreateSharedBitmap</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> whose data is shared with another resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3dbfe26f-cf36-47b0-925e-4934e0d7c390">CreateSolidColorBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new <a href="https://msdn.microsoft.com/a15c2696-3122-461e-806e-2195a50a3e92">ID2D1SolidColorBrush</a> that can be used to paint areas with a solid color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/241df698-ca5e-4d94-902a-a9e140820c14">DrawBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Draws the specified <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dabbb399-2d72-41c3-8b2f-aea49d7ad0cb">DrawEllipse</a>
</td>
<td align="left" width="63%">Overloaded. Draws the outline of an ellipse with the specified dimensions and stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/319b2680-34f8-4e00-985e-47ff87115794">DrawGeometry</a>
</td>
<td align="left" width="63%">
Draws the outline of the specified geometry using the specified stroke style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/064ede6c-139c-4160-9c50-460179d46f97">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
Draws the specified glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7eb70308-4142-4d32-a070-9e937579b896">DrawLine</a>
</td>
<td align="left" width="63%">
Draws a line between the specified points using the specified stroke style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f8c0754-fa68-4b5b-812f-24d8b544ba6e">DrawRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Draws the outline of a rectangle that has the specified dimensions and stroke style.
    

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d718c355-ffd8-4a7f-90f3-9a10d37a19c8">DrawRoundedRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Draws the outline of the specified rounded rectangle using the specified stroke style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cda7854-f9df-48d3-bc62-6aaee769e6f9">DrawText</a>
</td>
<td align="left" width="63%">Overloaded. Draws the specified text using the format information provided by an <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9356071a-35ca-462a-8a77-887e63850586">DrawTextLayout</a>
</td>
<td align="left" width="63%">
Draws the formatted text described by the specified <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a>
</td>
<td align="left" width="63%">
Ends drawing operations  on the render target and indicates the current error state and associated tags. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/149fb303-d2e8-416c-b28f-8bc5f1482ba6">FillEllipse</a>
</td>
<td align="left" width="63%">Overloaded. Paints the interior of the specified ellipse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/097f21ac-a062-4ce1-bdc7-87317dbdf5be">FillGeometry</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e22c9169-e770-4f3d-819b-b9363b6e6542">FillMesh</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified mesh.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5e56d8a-2929-4f7b-b1c4-fb358c202721">FillOpacityMask</a>
</td>
<td align="left" width="63%">Overloaded. Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08e498f9-b564-4da6-ba9b-bff08964ce08">FillRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Paints the interior of the specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c4765b0-858f-4a20-b044-0acf87a1f131">FillRoundedRectangle</a>
</td>
<td align="left" width="63%">Overloaded. Paints the interior of the specified rounded rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a>
</td>
<td align="left" width="63%">
Executes all pending drawing commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9aa93fa-0978-415e-b9f7-802494e81095">GetAntialiasMode</a>
</td>
<td align="left" width="63%">
Retrieves the current antialiasing mode for nontext drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72a25b78-96fd-42bf-9e71-6bb80efea0ac">GetDpi</a>
</td>
<td align="left" width="63%">
Return the render target's dots per inch (DPI).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55953177-4f81-4420-946a-ac03f1669c8f">GetMaximumBitmapSize</a>
</td>
<td align="left" width="63%">
Gets the maximum size, in device-dependent units (pixels), of  any one bitmap dimension supported by the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2dcd9af4-78d7-4271-9113-a91b4bb8145e">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format and alpha mode of the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0d736b5-0427-4c0d-8085-8498fd00f6b6">GetPixelSize</a>
</td>
<td align="left" width="63%">
Returns the size of the render target in device pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a46ec1c6-b0ff-4822-ab92-0b0a2ab564ba">GetSize</a>
</td>
<td align="left" width="63%">
Returns the size of the render target in device-independent pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71da439f-4666-4e49-93f8-26acd222ed1e">GetTags</a>
</td>
<td align="left" width="63%">
Gets the label for subsequent drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9d4ecd9-816d-43b2-adcf-25ac595279f4">GetTextAntialiasMode</a>
</td>
<td align="left" width="63%">
Gets the current antialiasing mode for text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/563a13c9-7f13-4b38-afa1-72e847dc8349">GetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Retrieves the render target's current text rendering options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ed0eded-ffbe-44f1-8fb0-b57f0cab7b70">GetTransform</a>
</td>
<td align="left" width="63%">
Gets the current transform of the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9fbc313-fe82-4425-9c9a-79bfacc08019">IsSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the render target supports the specified properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a>
</td>
<td align="left" width="63%">
Removes the last axis-aligned clip from the render target. After this method is called, the clip is no longer applied to subsequent drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a>
</td>
<td align="left" width="63%">
Stops redirecting drawing operations to the layer that is specified by the last <a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a> call. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b777425-07b1-4494-889a-0c947fb61315">PushAxisAlignedClip</a>
</td>
<td align="left" width="63%">Overloaded. Specifies a rectangle to which all subsequent drawing operations are clipped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9336662c-e94e-40ba-adbe-066d704958bc">PushLayer</a>
</td>
<td align="left" width="63%">Overloaded. Adds the specified layer to the render target so that it receives all subsequent drawing operations until <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> is called. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a>
</td>
<td align="left" width="63%">
Sets the render target's drawing state to that of the specified <a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a>
</td>
<td align="left" width="63%">
Saves the current drawing state to the specified <a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd727271-1725-48e1-be39-680b363db2ae">SetAntialiasMode</a>
</td>
<td align="left" width="63%">
Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/603a838b-4abc-4adf-93a9-ec8535d42ed6">SetDpi</a>
</td>
<td align="left" width="63%">
Sets the dots per inch (DPI) of the render target. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d71c3500-e11f-4b2d-9b78-b57df7dbc2bd">SetTags</a>
</td>
<td align="left" width="63%">
Specifies a label for subsequent drawing operations.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be6161ed-d797-4090-9bf0-5d6ee11cac0e">SetTextAntialiasMode</a>
</td>
<td align="left" width="63%">
Specifies the antialiasing mode to use for subsequent text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab4b29a5-72a7-49dc-9131-696f888b0355">SetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Specifies text rendering options to be applied to all subsequent text and glyph drawing operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04799366-6458-40ff-a2fb-5d227eab041d">SetTransform</a>
</td>
<td align="left" width="63%">Overloaded. Applies the specified transform to the render target, replacing the existing transformation. All subsequent drawing operations occur in the transformed space.

</td>
</tr>
</table> 


## -remarks



Your application should create render targets once and hold onto them for the life of the application or until the render target's  <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> method returns the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created). 




## -see-also




<a href="https://msdn.microsoft.com/b1362ef6-40fc-4fa5-ba5b-22c622c39f04">Direct2D API Overview</a>



<a href="https://msdn.microsoft.com/48aae6dd-0f23-43ab-9deb-e6f42c57be4a">Getting Started</a>



<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

