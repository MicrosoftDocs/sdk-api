---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInkOverlay::get_DefaultDrawingAttributes


## -description



Gets or sets the default drawing attributes to use when drawing and displaying ink.



This property is read/write.


## -parameters


## -remarks



The drawing attributes specified with this property are the attributes that are assigned to a new cursor.

The default drawing attributes are as follows:


<a href="https://msdn.microsoft.com/3536cd42-372d-4bd7-ac69-ef8d6c07f7fd">AntiAliased</a> = <b>TRUE</b>


<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> = <b>BLACK</b> (RGB(0,0,0)) if not in High Contrast mode; otherwise, Color=COLOR_WINDOWTEXT.


<a href="https://msdn.microsoft.com/93b11903-84dd-4f7a-a47c-555d19fede8d">FitToCurve</a> = <b>FALSE</b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff542686">Height</a> = 1 (in ink space units)


<a href="https://msdn.microsoft.com/adf5beec-75df-46a3-91e4-33595340aca2">IgnorePressure</a> = <b>FALSE</b>


<a href="https://msdn.microsoft.com/13e3c2dc-99a4-4643-b8b2-48586b0eb2f0">PenTip</a> = <b>Ball</b>


<a href="https://msdn.microsoft.com/8e3681a7-c5be-4104-b740-9f23d141f6cb">RasterOperation</a> = <b>CopyPen</b>


<a href="https://msdn.microsoft.com/e1537635-3457-429e-bb72-33eb4a2ea3da">Transparency</a> = 0 (totally opaque)


<a href="https://msdn.microsoft.com/library/windows/hardware/ff553316">Width</a> = 53 (in ink space units)

To set different attributes on a new cursor, use the <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property of the <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> object.

To change the drawing attributes of a single stroke, use the <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object. To change the drawing attributes of a collection of strokes, call the <a href="https://msdn.microsoft.com/b249edd9-dfa4-4538-9764-a4365f9df527">ModifyDrawingAttributes</a> method of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a> property contains the drawing attributes that all cursors use unless they set their own <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property. For example, a new <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> object uses <b>DefaultDrawingAttributes</b>, and an old <b>IInkCursor</b> object on which the <b>DrawingAttributes</b> is set to <b>NULL</b> also uses <b>DefaultDrawingAttributes</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor Interface</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>



<a href="https://msdn.microsoft.com/b249edd9-dfa4-4538-9764-a4365f9df527">ModifyDrawingAttributes Method</a>
 

 

