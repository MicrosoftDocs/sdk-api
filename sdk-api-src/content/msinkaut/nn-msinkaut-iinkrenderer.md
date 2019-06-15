---
UID: NN:msinkaut.IInkRenderer
title: IInkRenderer (msinkaut.h)
author: windows-sdk-content
description: "."
old-location: tablet\iinkrenderer.htm
tech.root: tablet
ms.assetid: 2AB56616-3F67-4428-8A99-FCE733A5FDBF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkRenderer, IInkRenderer interface [Tablet PC], IInkRenderer interface [Tablet PC],described, msinkaut/IInkRenderer, tablet.iinkrenderer
ms.topic: interface
f1_keywords: ["msinkaut/IInkRenderer"]
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkRenderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRenderer interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRenderer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInkRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw">Draw</a>
</td>
<td align="left" width="63%">
Draws ink strokes using the known device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a>
</td>
<td align="left" width="63%">
Draws the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object using the known device context, and optionally draws the <b>IInkStrokeDisp</b> object with the known <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform">GetObjectTransform</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the object transform that was used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">GetViewTransform</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the view transform that is used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel">InkSpaceToPixel</a>
</td>
<td align="left" width="63%">
Converts a location in ink space  coordinates to a location in pixel space using a handle for the conversion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints">InkSpaceToPixelFromPoints</a>
</td>
<td align="left" width="63%">
Converts an array of points in ink space coordinates to an array of points in pixel space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure">Measure</a>
</td>
<td align="left" width="63%">
Calculates the rectangle on the device context that would contain a collection of strokes if the strokes were drawn with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object using the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke">MeasureStroke</a>
</td>
<td align="left" width="63%">
Calculates the rectangle on the device context that would contain a stroke if it were drawn with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object using the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move">Move</a>
</td>
<td align="left" width="63%">
Applies a translation to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">view transform</a> in ink space coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace">PixelToInkSpace</a>
</td>
<td align="left" width="63%">
Converts a location in pixel space coordinates to be a location in ink space coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints">PixelToInkSpaceFromPoints</a>
</td>
<td align="left" width="63%">
Converts an array of locations in pixel space coordinates to an array of locations in ink space  coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate">Rotate</a>
</td>
<td align="left" width="63%">
Applies a rotation to a <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrenderer-class">InkRenderer</a>'s view transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform">ScaleTransform</a>
</td>
<td align="left" width="63%">
Scales the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform">view transform</a> in the X and Y dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform">SetObjectTransform</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the object transform that is used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform">SetViewTransform</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object that represents the view transform that is used to render ink.

</td>
</tr>
</table> 

