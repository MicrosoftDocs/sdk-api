---
UID: NF:msinkaut.IInkStrokeDisp.get_DrawingAttributes
title: IInkStrokeDisp::get_DrawingAttributes method
author: windows-driver-content
description: Gets or sets the drawing attributes to apply to ink as it is drawn.
old-location: tablet\iinkstrokedisp_drawingattributes.htm
old-project: tablet
ms.assetid: f41de939-0c20-4128-bee4-22a0c434159f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC], IInkStrokeDisp interface, IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], DrawingAttributes property, IInkStrokeDisp.DrawingAttributes, IInkStrokeDisp.get_DrawingAttributes, IInkStrokeDisp.put_DrawingAttributes, IInkStrokeDisp::get_DrawingAttributes, IInkStrokeDisp::put_DrawingAttributes, get_DrawingAttributes,IInkStrokeDisp.get_DrawingAttributes, msinkaut/IInkStrokeDisp::DrawingAttributes, msinkaut/IInkStrokeDisp::get_DrawingAttributes, msinkaut/IInkStrokeDisp::put_DrawingAttributes, tablet.iinkstrokedisp_drawingattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.DrawingAttributes
-	IInkStrokeDisp.get_DrawingAttributes
-	IInkStrokeDisp.put_DrawingAttributes
-	IInkStrokeDisp.get_DrawingAttributes
-	IInkStrokeDisp.put_DrawingAttributes
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkStrokeDisp::get_DrawingAttributes method


## -description



Gets or sets the drawing attributes to apply to ink as it is drawn.



This property is read/write.


## -parameters


## -remarks



The drawing attributes specify the appearance of the stroke. For example, you can specify the style and color of a pen.

A cursor can have different drawing attributes for each <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> with which it comes in contact. If you do not specify drawing attributes for a cursor, it uses the default drawing attributes of the <b>InkCollector</b> object. These default attributes are set with the <a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a> property of the <b>InkCollector</b> object.

Successive calls to the <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property change only the drawing attributes of new strokes. They do not apply to strokes that are already collected or being collected.

<div class="alert"><b>Note</b>  This property behaves differently than the <a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a> property. Although the <b>DefaultDrawingAttributes</b> property specifies the drawing attributes that are applied to a new cursor, the <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property specifies the drawing attributes for ink that is yet to be collected.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>
 

 

