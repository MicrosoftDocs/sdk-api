---
UID: NF:oleidl.IViewObject.Draw
title: IViewObject::Draw (oleidl.h)
description: Draws a representation of an object onto the specified device context.
helpviewer_keywords: ["Draw","Draw method [COM]","Draw method [COM]","IViewObject interface","IViewObject interface [COM]","Draw method","IViewObject.Draw","IViewObject::Draw","_ole_iviewobject_draw","com.iviewobject_draw","oleidl/IViewObject::Draw"]
old-location: com\iviewobject_draw.htm
tech.root: com
ms.assetid: 913593ff-07fe-44bd-88dc-8e58da82089b
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [COM], Draw method [COM],IViewObject interface, IViewObject interface [COM],Draw method, IViewObject.Draw, IViewObject::Draw, _ole_iviewobject_draw, com.iviewobject_draw, oleidl/IViewObject::Draw
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IViewObject::Draw
 - oleidl/IViewObject::Draw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IViewObject.Draw
---

# IViewObject::Draw


## -description

Draws a representation of an object onto the specified device context.

## -parameters

### -param dwDrawAspect [in]

Specifies the aspect to be drawn, that is, how the object is to be represented. Representations include content, an icon, a thumbnail, or a printed document. Valid values are taken from the enumerations <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> and <a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>. Note that newer objects and containers that support optimized drawing interfaces support the <b>DVASPECT2</b> enumeration values. Older objects and containers that do not support optimized drawing interfaces may not support <b>DVASPECT2</b>. Windowless objects allow only <b>DVASPECT</b>_CONTENT, <b>DVASPECT</b>_OPAQUE, and <b>DVASPECT</b>_TRANSPARENT.

### -param lindex [in]

Portion of the object that is of interest for the draw operation. Its interpretation varies depending on the value in the dwAspect parameter. See the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration for more information.

### -param pvAspect [in]

Pointer to additional information in a <a href="/windows/win32/api/ocidl/ns-ocidl-dvaspectinfo">DVASPECTINFO</a> structure that enables drawing optimizations depending on the aspect specified. Note that newer objects and containers that support optimized drawing interfaces support this parameter as well. Older objects and containers that do not support optimized drawing interfaces always specify <b>NULL</b> for this parameter.

### -param ptd [in]

Pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure that describes the device for which the object is to be rendered. If <b>NULL</b>, the view should be rendered for the default target device (typically the display). A value other than <b>NULL</b> is interpreted in conjunction with <i>hdcTargetDev</i> and <i>hdcDraw</i>. For example, if <i>hdcDraw</i> specifies a printer as the device context, the <i>ptd</i> parameter points to a structure describing that printer device. The data may actually be printed if <i>hdcTargetDev</i> is a valid value or it may be displayed in print preview mode if <i>hdcTargetDev</i> is <b>NULL</b>.

### -param hdcTargetDev [in]

Information context for the target device indicated by the ptd parameter from which the object can extract device metrics and test the device's capabilities. If <i>ptd</i> is <b>NULL</b>; the object should ignore the value in the <i>hdcTargetDev</i> parameter.

### -param hdcDraw [in]

Device context on which to draw. For a windowless object, the <i>hdcDraw</i> parameter should be in MM_TEXT mapping mode with its logical coordinates matching the client coordinates of the containing window. For a windowless object, the device context should be in the same state as the one normally passed by a WM_PAINT message.

### -param lprcBounds [in]

Pointer to a RECTL structure specifying the rectangle on <i>hdcDraw</i> and in which the object should be drawn. This parameter controls the positioning and stretching of the object. This parameter should be <b>NULL</b> to draw a windowless in-place active object. In every other situation, <b>NULL</b> is not a legal value and should result in an E_INVALIDARG error code. If the container passes a non-<b>NULL</b> value to a windowless object, the object should render the requested aspect into the specified device context and rectangle. A container can request this from a windowless object to render a second, non-active view of the object or to print the object.

### -param lprcWBounds [in]

If <i>hdcDraw</i> is a metafile device context, pointer to a RECTL structure specifying the bounding rectangle in the underlying metafile. The rectangle structure contains the window extent and window origin. These values are useful for drawing metafiles. The rectangle indicated by <i>lprcBounds</i> is nested inside this <i>lprcWBounds</i> rectangle; they are in the same coordinate space.

If <i>hdcDraw</i> is not a metafile device context; <i>lprcWBounds</i> will be <b>NULL</b>.

### -param pfnContinue [in]

Pointer to a callback function that the view object should call periodically during a lengthy drawing operation to determine whether the operation should continue or be canceled. This function returns <b>TRUE</b> to continue drawing. It returns <b>FALSE</b> to stop the drawing in which case <b>IViewObject::Draw</b> returns DRAW_E_ABORT.



#### dwContinue

### -param dwContinue [in]

Value to pass as a parameter to the function pointed to by the <i>pfnContinue</i> parameter. Typically, <i>dwContinue</i> is a pointer to an application-defined structure needed inside the callback function.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
No data to draw from.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAW_E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Draw operation aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIEW_E_DRAW</b></dt>
</dl>
</td>
<td width="60%">
Error in drawing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for lindex; currently only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>dwAspect</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_INVALIDRECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid rectangle.

</td>
</tr>
</table>

## -remarks

A container application issues a call to <b>IViewObject::Draw</b> to create a representation of a contained object. This method draws the specified piece (<i>lindex</i>) of the specified view (<i>dwAspect</i> and <i>pvAspect</i>) on the specified device context (<i>hdcDraw</i>). Formatting, fonts, and other rendering decisions are made on the basis of the target device specified by the ptd parameter.

There is a relationship between the <i>dwDrawAspect</i> value and the <i>lprcbounds</i> value. The <i>lprcbounds</i> value specifies the rectangle on <i>hdcDraw</i> into which the drawing is to be mapped. For <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>_THUMBNAIL, <b>DVASPECT</b>_ICON, and <b>DVASPECT</b>_SMALLICON, the object draws whatever it wants to draw, and it maps it into the space given in the best way. Some objects might scale to fit while some might scale to fit but preserve the aspect ratio. In addition, some might scale so the drawing appears at full width, but the bottom is cropped. The container can suggest a size via <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">IOleObject::SetExtent</a>, but it has no control over the rendering size. In the case of <b>DVASPECT</b>_CONTENT, the <b>IViewObject::Draw</b> implementation should either use the extents given by <b>IOleObject::SetExtent</b> or use the bounding rectangle given in the <i>lprcBounds</i> parameter.

For newer objects that support optimized drawing techniques and for windowless objects, this method should be used as follows:

<ul>
<li>New drawing aspects are supported in <i>dwAspect</i> as defined in <a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>.</li>
<li>The pvAspect parameter can be used to pass additional information allowing drawing optimizations through the <a href="/windows/win32/api/ocidl/ns-ocidl-dvaspectinfo">DVASPECTINFO</a> structure.</li>
<li>The <b>IViewObject::Draw</b> method can be called to redraw a windowless in-place active object by setting the <i>lrpcBounds</i> parameter to <b>NULL</b>. In every other situation, <b>NULL</b> is an illegal value and should result in an E_INVALIDARG error code. A windowless object uses the rectangle passed by the activation verb or calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects">IOleInPlaceObject::SetObjectRects</a> instead of using this parameter. If the container passes a non-<b>NULL</b> value to a windowless object, the object should render the requested aspect into the specified device context and rectangle. A container can request this from a windowless object to render a second, non-active view of the object or to print the object. See the <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a> interface for more information on drawing windowless objects.</li>
<li>For windowless objects, the <i>dwAspect</i> parameter only allows the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>_CONTENT, <b>DVASPECT</b>_OPAQUE, and <b>DVASPECT</b>_TRANSPARENT aspects.</li>
<li>For a windowless object, the hdcDraw parameter should be in MM_TEXT mapping mode with its logical coordinates matching the client coordinates of the containing window. For a windowless object, the device context should be in the same state as the one normally passed by a WM_PAINT message.</li>
</ul>
To maintain compatibility with older objects and containers that do not support drawing optimizations, all objects, rectangular or not, are required to maintain an origin and a rectangular extent. This allows the container to still consider all its embedded objects as rectangles and to pass them appropriate rendering rectangles in <b>Draw</b>.

An object's extent depends on the drawing aspect. For non-rectangular objects, the extent should be the size of a rectangle covering the entire aspect. By convention, the origin of an object is the top-left corner of the rectangle of the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>_CONTENT aspect. In other words, the origin always coincides with the top-left corner of the rectangle maintained by the object's site, even for a non-rectangular object.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>



<a href="/windows/win32/api/ocidl/ns-ocidl-dvaspectinfo">DVASPECTINFO</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplacesitewindowless">IOleInPlaceSiteWindowless</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/ole/nf-ole-oledraw">OleDraw</a>