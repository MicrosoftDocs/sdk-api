---
UID: NN:d2d1_1.ID2D1DeviceContext
title: ID2D1DeviceContext
author: windows-sdk-content
description: Represents a set of state and command buffers that are used to render to a target.
old-location: direct2d\id2d1devicecontext.htm
tech.root: direct2d
ms.assetid: a54dd628-c2a2-4b04-9ced-7749a395f187
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1DeviceContext, ID2D1DeviceContext interface [Direct2D], ID2D1DeviceContext interface [Direct2D],described, d2d1_1/ID2D1DeviceContext, direct2d.id2d1devicecontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext interface


## -description


Represents a set of state and command buffers that are used to render to a target.

The device context can render to a target bitmap or a command list.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext</b> interface inherits from <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>. <b>ID2D1DeviceContext</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D1896DEE-4464-48D7-8EFB-18E564E1F88D">CreateBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the <a href="https://msdn.microsoft.com/e6cff1b7-055b-442c-99aa-afeeee4d06e8">DrawBitmap</a> and <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> APIs. In addition, color context information can be passed to the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1573F748-7726-4DC7-BBBA-83A7538A1AF8">CreateBitmapBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates a bitmap brush, the input image is a Direct2D bitmap object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/JJ841135(v=VS.85).aspx">CreateBitmapFromDxgiSurface</a>
</td>
<td align="left" width="63%">Overloaded.  Creates a bitmap from a DXGI surface that can be set as a target surface or have additional color context information specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE1AC711-8DD2-47F8-B1D5-CBCCC3F298B8">CreateBitmapFromWicBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Creates a Direct2D bitmap by copying a WIC bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e03dfe6-b114-46da-820e-341c554b178b">CreateColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae72c68a-d984-4287-b607-a18913f083d4">CreateColorContextFromFilename</a>
</td>
<td align="left" width="63%">
Creates a color context by loading it from the specified filename.  The profile bytes are the contents of the file specified by <i>Filename</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaa97544-f767-4a46-95bc-528e484fd24f">CreateColorContextFromWicColorContext</a>
</td>
<td align="left" width="63%">
Creates a color context from an <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.  The <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">D2D1ColorContext</a> space of the resulting context varies, see Remarks for more info.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f34710dc-7845-457f-9b27-51ae937d9f74">CreateCommandList</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">CreateEffect</a>
</td>
<td align="left" width="63%">
Creates an effect for the specified class ID. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6374fc62-1f54-4112-8ba3-9c1167bf8685">CreateGradientStopCollection</a>
</td>
<td align="left" width="63%">
Creates a gradient stop collection, enabling the gradient to contain color channels with values outside of [0,1] and also enabling rendering to a high-color render target with interpolation in sRGB space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81C609EC-7545-4A23-B6DD-00DF70141C27">CreateImageBrush</a>
</td>
<td align="left" width="63%">Overloaded. Creates an image brush. The input image can be any type of image, including a bitmap, effect, or a command list.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79F75156-5BFB-4B00-BFE1-709724AAA459">DrawBitmap</a>
</td>
<td align="left" width="63%">Overloaded. Draws a bitmap to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57A08FFE-7B2D-477F-AEAD-E6A315B5B932">DrawGdiMetafile</a>
</td>
<td align="left" width="63%">Overloaded. Draw a metafile to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a169604c-64d6-401f-83f5-fb322230e110">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
Draws a series of glyphs to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DDB355F0-04CD-4B39-9E96-7020F47B0392">DrawImage</a>
</td>
<td align="left" width="63%">Overloaded. Draws an image to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79844FCE-BD42-4F57-B51B-A0ECC490A471">FillOpacityMask</a>
</td>
<td align="left" width="63%">Overloaded. Fill using the alpha channel of the supplied opacity mask bitmap. The brush opacity will be modulated by the mask. The render target antialiasing mode must be set to aliased.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c8664cb-d6be-41e0-8415-d60dcd46132a">GetDevice</a>
</td>
<td align="left" width="63%">
Gets the device associated with a device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C0B70DA1-C9BF-47AC-BF3E-2A741DACD2E8">GetEffectInvalidRectangleCount</a>
</td>
<td align="left" width="63%">
Gets the number of invalid output rectangles that have accumulated on the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5CEFDB0-BD54-4CB9-801C-528CDA49C19C">GetEffectInvalidRectangles</a>
</td>
<td align="left" width="63%">
Gets the invalid rectangles that have accumulated since the last time the effect was drawn and <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> was then called on the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B34548A9-1E23-496F-A1D9-87B74EF67C72">GetEffectRequiredInputRectangles</a>
</td>
<td align="left" width="63%">
Returns the input rectangles that are required to be supplied by the caller to produce the given output rectangle. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1196095A-4B26-4E71-A7F4-86F23B79E1F6">GetGlyphRunWorldBounds</a>
</td>
<td align="left" width="63%">
    Gets the world-space bounds in DIPs of the glyph run using the device
    context DPI. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a0f4e36-4490-4df5-a520-e10e524c8337">GetImageLocalBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of an image without the world transform of the context applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/939531E1-B641-48EF-B129-AC3AA5226919">GetImageWorldBounds</a>
</td>
<td align="left" width="63%">
Gets the bounds of an image with the world transform of the context applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3d6cfae-5776-4d1d-933b-b94271c431b6">GetPrimitiveBlend</a>
</td>
<td align="left" width="63%">
Returns the currently set primitive blend used by the device context.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1d15530-a525-42ba-bc58-f8f429cdd2a8">GetRenderingControls</a>
</td>
<td align="left" width="63%">
Gets the rendering controls that have been applied to the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a70307db-863a-4c59-a327-fb71a5d58f84">GetTarget</a>
</td>
<td align="left" width="63%">
Gets the target currently associated with the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1c6476d-151b-4f2a-9aae-726de219567c">GetUnitMode</a>
</td>
<td align="left" width="63%">
Gets the mode that  is being used to interpret values by the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3EB22E7B-69B4-4936-B8ED-093EA1EA1759">InvalidateEffectInputRectangle</a>
</td>
<td align="left" width="63%">
This indicates that a portion of an effect's input is invalid. This method can
     be called many times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c65824dc-a9d5-4d4d-a2de-b4283153f64f">IsBufferPrecisionSupported</a>
</td>
<td align="left" width="63%">
Indicates whether the buffer precision is supported by the underlying Direct3D <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">device.</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA70292A-7B1C-4916-91CA-80263839BC3F">IsDxgiFormatSupported</a>
</td>
<td align="left" width="63%">
 Indicates whether the format is supported by the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DC719E3-CE94-4B7F-B02D-62D78425CFFE">PushLayer</a>
</td>
<td align="left" width="63%">
Push a layer onto the clip and layer stack of the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be04c9f7-397f-468e-91c0-3b11c68b489f">SetPrimitiveBlend</a>
</td>
<td align="left" width="63%">
Changes the primitive blend mode that is used for all rendering operations in the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a066126-89d0-4372-bc01-6b6fa1d65440">SetRenderingControls</a>
</td>
<td align="left" width="63%">
Sets the rendering controls for the given device context. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66914048-7bef-4551-bb14-5ab67c727dc5">SetTarget</a>
</td>
<td align="left" width="63%">
The bitmap or command list to which the <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device context will now render.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5774b9a-4458-47e7-821a-4ac4b70468e3">SetUnitMode</a>
</td>
<td align="left" width="63%">
Sets what units will be used to interpret values passed into the device context.

</td>
</tr>
</table> 


## -remarks



 Any resource created from a device context can be shared with any other resource created from a device context when both contexts are created on the same device. 




## -see-also




<a href="https://msdn.microsoft.com/0e56d057-20a5-47b7-aec9-63c8e31f349b">D2D1CreateDeviceContext</a>



<a href="https://msdn.microsoft.com/D4563FEA-767E-4B16-8F3C-3D548A64B206">Devices and Device Contexts</a>



<a href="https://msdn.microsoft.com/d14255d4-ae59-42b4-ada9-bd7a3c5e8024">ID2D1Device::CreateDeviceContext</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

