---
UID: NN:d2d1_1.ID2D1CommandSink
title: ID2D1CommandSink
author: windows-sdk-content
description: The command sink is implemented by you for an application when you want to receive a playback of the commands recorded in a command list.
old-location: direct2d\id2d1commandsink.htm
tech.root: Direct2D
ms.assetid: 4e0ce837-7f4e-4b93-8dd7-68f60cfb1105
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID2D1CommandSink, ID2D1CommandSink interface [Direct2D], ID2D1CommandSink interface [Direct2D],described, d2d1_1/ID2D1CommandSink, direct2d.id2d1commandsink
ms.prod: windows
ms.technology: windows-sdk
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
 - ID2D1CommandSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink interface


## -description



The command sink is implemented by you for an application when you want to receive a playback of the commands recorded in a command list. A typical usage will be for transforming the command list into another format such as XPS when some degree of conversion between the <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> primitives and the target format is required.



The command sink interface doesn't have any resource creation methods on it. The resources are still logically bound to the <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device on which the command list was created and will be passed in to the command sink implementation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1CommandSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1CommandSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1CommandSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acadc36f-5028-4f8f-93c6-7fbc0de3c3d5">BeginDraw</a>
</td>
<td align="left" width="63%">
Notifies the implementation of the command sink that drawing is about to commence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d91bb6b2-ecc8-4c16-95fc-c0cb7bbe80e3">Clear</a>
</td>
<td align="left" width="63%">
Clears the drawing area to the specified color. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95F73EBD-989E-4FB1-B1D2-86642E99FA3E">DrawBitmap</a>
</td>
<td align="left" width="63%">
Draws a bitmap to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D986C99-BB7D-4A46-A147-E907F1031E92">DrawGdiMetafile</a>
</td>
<td align="left" width="63%">
Draw a metafile to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff91dd6c-0604-44aa-a30c-6b531cc3fb58">DrawGeometry</a>
</td>
<td align="left" width="63%">
Indicates the geometry to be drawn to the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b40a999-0046-458e-b7bc-95037d73833c">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
Indicates the glyphs to be drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1235dd6d-8495-4a92-96b7-4d741d9e296f">DrawImage</a>
</td>
<td align="left" width="63%">
Draws the provided image to the command sink.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c47b5af-d258-42f8-b329-eb28d9485d3a">DrawLine</a>
</td>
<td align="left" width="63%">
Draws a line drawn between two points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93c617fb-3c9d-4735-a077-7a3a58033369">DrawRectangle</a>
</td>
<td align="left" width="63%">
Draws a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7324d66b-b415-4e07-9fe3-d79a1c0a49b0">EndDraw</a>
</td>
<td align="left" width="63%">
Indicates when  <b>ID2D1CommandSink</b> processing has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04e93b19-f3a7-4196-bce0-e656d48116ef">FillGeometry</a>
</td>
<td align="left" width="63%">
Indicates to the command sink a geometry to be filled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b81ac1d2-06bb-4d39-b03d-c0abf7267c3a">FillMesh</a>
</td>
<td align="left" width="63%">
Indicates a mesh to be filled by the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c125b2db-0786-4bda-b31f-de05ba72afa1">FillOpacityMask</a>
</td>
<td align="left" width="63%">
Fills an opacity mask on the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c970a962-8d03-4de8-9252-9babfa411e5f">FillRectangle</a>
</td>
<td align="left" width="63%">
Indicates to the command sink a rectangle to be filled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/602cede8-dce1-4032-b099-b8088bc57459">PopAxisAlignedClip</a>
</td>
<td align="left" width="63%">
Removes an axis-aligned clip from the layer and clip stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/885fb53b-da63-4c46-8ca2-306fd430858b">PopLayer</a>
</td>
<td align="left" width="63%">
Removes  a layer from the layer and clip stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09e20780-2ebd-417e-9953-421f49dba4dd">PushAxisAlignedClip</a>
</td>
<td align="left" width="63%">
Pushes a clipping rectangle onto the clip and layer stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/071d7d7a-12d7-4611-812c-103e2b9a5e56">PushLayer</a>
</td>
<td align="left" width="63%">
Pushes a layer onto the clip and layer stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/335cb9e7-56da-4971-b6d1-94292a6a771a">SetAntialiasMode</a>
</td>
<td align="left" width="63%">
Sets the antialiasing mode that will be used to render any subsequent geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80b7047f-1200-4dc9-bc64-96678524a449">SetPrimitiveBlend</a>
</td>
<td align="left" width="63%">
Sets a new primitive blend mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56898541-8c4a-4dbb-aa34-cc957b1f17ff">SetTags</a>
</td>
<td align="left" width="63%">
Sets the tags that correspond to the tags in the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6bd9c50-b0a5-4d5e-b554-1c4caa6d8e00">SetTextAntialiasMode</a>
</td>
<td align="left" width="63%">
Indicates the new default antialiasing mode for text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e847f2e3-6d2d-45e6-b1ef-bf393ed53e2b">SetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Indicates more detailed text rendering parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc284b13-cf22-45aa-b80c-0750622f5284">SetTransform</a>
</td>
<td align="left" width="63%">
Sets a new transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e524aa51-2499-4333-9562-a4893666b666">SetUnitMode</a>
</td>
<td align="left" width="63%">
The unit mode changes the meaning of subsequent units from DIPs to pixels  or the other way. The command sink does not record a DPI, this is implied by the playback context or other playback interface such as <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a>.

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1CommandSink</b> can be implemented to receive a play-back of the commands recorded in a command list. This interface is typically used for transforming the command list into another format  where some degree of conversion between the Direct2D primitives and the target format is required.
      
      

The <b>ID2D1CommandSink</b> interface does not have any resource creation methods. The resources are logically bound to the Direct2D device on which the <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> was created and will be passed in to the <b>ID2D1CommandSink</b> implementation.
      
      

Not all methods implemented by <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a> are present.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

