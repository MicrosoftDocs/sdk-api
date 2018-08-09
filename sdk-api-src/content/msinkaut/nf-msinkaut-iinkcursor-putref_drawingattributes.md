---
UID: NF:msinkaut.IInkCursor.putref_DrawingAttributes
title: IInkCursor::putref_DrawingAttributes
author: windows-sdk-content
description: Gets or sets the drawing attributes to apply to ink as it is drawn.
old-location: tablet\iinkcursor_drawingattributes.htm
old-project: tablet
ms.assetid: de8b2473-092d-4ff9-adbc-3ba378b035e2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC],IInkCursor interface, IInkCursor interface [Tablet PC],DrawingAttributes property, IInkCursor.DrawingAttributes, IInkCursor.get_DrawingAttributes, IInkCursor.putref_DrawingAttributes, IInkCursor::DrawingAttributes, IInkCursor::get_DrawingAttributes, IInkCursor::putref_DrawingAttributes, de8b2473-092d-4ff9-adbc-3ba378b035e2, msinkaut/IInkCursor::DrawingAttributes, msinkaut/IInkCursor::get_DrawingAttributes, msinkaut/IInkCursor::putref_DrawingAttributes, putref_DrawingAttributes, tablet.iinkcursor_drawingattributes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCursor.DrawingAttributes
 - IInkCursor.get_DrawingAttributes
 - IInkCursor.get_DrawingAttributes
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCursor::putref_DrawingAttributes


## -description



Gets or sets the drawing attributes to apply to ink as it is drawn.



This property is read/write.


## -parameters


## -remarks



The drawing attributes specify the appearance of the stroke. For example, you can specify the style and color of a pen.

A cursor can have different drawing attributes for each <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> with which it comes in contact. If you do not specify drawing attributes for a cursor, it uses the default drawing attributes of the <b>InkCollector</b> object. These default attributes are set with the <a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a> property of the <b>InkCollector</b> object.

Successive calls to the <b>DrawingAttributes</b> property change only the drawing attributes of new strokes. They do not apply to strokes that are already collected or being collected.

<div class="alert"><b>Note</b>  This property behaves differently than the <a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a> property. Although the <b>DefaultDrawingAttributes</b> property specifies the drawing attributes that are applied to a new cursor, the <b>DrawingAttributes</b> property specifies the drawing attributes for ink that is yet to be collected.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">InkCursor Interface</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>
 

 

