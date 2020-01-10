---
UID: NN:d2d1_1.ID2D1CommandSink
title: ID2D1CommandSink (d2d1_1.h)
description: The command sink is implemented by you for an application when you want to receive a playback of the commands recorded in a command list.
old-location: direct2d\id2d1commandsink.htm
tech.root: Direct2D
ms.assetid: 4e0ce837-7f4e-4b93-8dd7-68f60cfb1105
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink, ID2D1CommandSink interface [Direct2D], ID2D1CommandSink interface [Direct2D],described, d2d1_1/ID2D1CommandSink, direct2d.id2d1commandsink
f1_keywords:
- d2d1_1/ID2D1CommandSink
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1CommandSink interface


## -description



The command sink is implemented by you for an application when you want to receive a playback of the commands recorded in a command list. A typical usage will be for transforming the command list into another format such as XPS when some degree of conversion between the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> primitives and the target format is required.



The command sink interface doesn't have any resource creation methods on it. The resources are still logically bound to the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device on which the command list was created and will be passed in to the command sink implementation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1CommandSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1CommandSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-begindraw">BeginDraw</a>
</td>
<td align="left" width="63%">
Notifies the implementation of the command sink that drawing is about to commence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the drawing area to the specified color. 



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawbitmap">DrawBitmap</a>
</td>
<td align="left" width="63%">
Draws a bitmap to the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawgdimetafile">DrawGdiMetafile</a>
</td>
<td align="left" width="63%">
Draw a metafile to the device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawgeometry">DrawGeometry</a>
</td>
<td align="left" width="63%">
Indicates the geometry to be drawn to the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawglyphrun">DrawGlyphRun</a>
</td>
<td align="left" width="63%">
Indicates the glyphs to be drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawimage">DrawImage</a>
</td>
<td align="left" width="63%">
Draws the provided image to the command sink.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawline">DrawLine</a>
</td>
<td align="left" width="63%">
Draws a line drawn between two points.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawrectangle">DrawRectangle</a>
</td>
<td align="left" width="63%">
Draws a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-enddraw">EndDraw</a>
</td>
<td align="left" width="63%">
Indicates when  <b>ID2D1CommandSink</b> processing has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillgeometry">FillGeometry</a>
</td>
<td align="left" width="63%">
Indicates to the command sink a geometry to be filled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillmesh">FillMesh</a>
</td>
<td align="left" width="63%">
Indicates a mesh to be filled by the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask">FillOpacityMask</a>
</td>
<td align="left" width="63%">
Fills an opacity mask on the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillrectangle">FillRectangle</a>
</td>
<td align="left" width="63%">
Indicates to the command sink a rectangle to be filled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-popaxisalignedclip">PopAxisAlignedClip</a>
</td>
<td align="left" width="63%">
Removes an axis-aligned clip from the layer and clip stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-poplayer">PopLayer</a>
</td>
<td align="left" width="63%">
Removes  a layer from the layer and clip stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushaxisalignedclip">PushAxisAlignedClip</a>
</td>
<td align="left" width="63%">
Pushes a clipping rectangle onto the clip and layer stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer">PushLayer</a>
</td>
<td align="left" width="63%">
Pushes a layer onto the clip and layer stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-setantialiasmode">SetAntialiasMode</a>
</td>
<td align="left" width="63%">
Sets the antialiasing mode that will be used to render any subsequent geometry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-setprimitiveblend">SetPrimitiveBlend</a>
</td>
<td align="left" width="63%">
Sets a new primitive blend mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-settags">SetTags</a>
</td>
<td align="left" width="63%">
Sets the tags that correspond to the tags in the command sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-settextantialiasmode">SetTextAntialiasMode</a>
</td>
<td align="left" width="63%">
Indicates the new default antialiasing mode for text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-settextrenderingparams">SetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Indicates more detailed text rendering parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-settransform">SetTransform</a>
</td>
<td align="left" width="63%">
Sets a new transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-setunitmode">SetUnitMode</a>
</td>
<td align="left" width="63%">
The unit mode changes the meaning of subsequent units from DIPs to pixels  or the other way. The command sink does not record a DPI, this is implied by the playback context or other playback interface such as <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a>.

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1CommandSink</b> can be implemented to receive a play-back of the commands recorded in a command list. This interface is typically used for transforming the command list into another format  where some degree of conversion between the Direct2D primitives and the target format is required.
      
      

The <b>ID2D1CommandSink</b> interface does not have any resource creation methods. The resources are logically bound to the Direct2D device on which the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> was created and will be passed in to the <b>ID2D1CommandSink</b> implementation.
      
      

Not all methods implemented by <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> are present.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

