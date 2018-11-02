---
UID: NF:inked.IInkEdit.putref_DrawingAttributes
title: IInkEdit::putref_DrawingAttributes
author: windows-sdk-content
description: Gets or sets the drawing attributes for ink that is yet to be drawn on the InkEdit control.
old-location: tablet\inkedit_drawingattributes.htm
tech.root: tablet
ms.assetid: 8f5f00a2-abe1-487e-a067-2b6d929824c7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 8f5f00a2-abe1-487e-a067-2b6d929824c7, DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],DrawingAttributes property, IInkEdit.DrawingAttributes, IInkEdit.putref_DrawingAttributes, IInkEdit::DrawingAttributes, IInkEdit::get_DrawingAttributes, IInkEdit::putref_DrawingAttributes, InkEdit.get_DrawingAttributes, get_DrawingAttributes, inked/IInkEdit::DrawingAttributes, inked/IInkEdit::get_DrawingAttributes, inked/IInkEdit::putref_DrawingAttributes, put_DrawingAttributes, putref_DrawingAttributes, tablet.inkedit_drawingattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: inked.h
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
req.lib: InkEd.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.DrawingAttributes
 - IInkEdit.get_DrawingAttributes
 - InkEdit.get_DrawingAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkEdit::putref_DrawingAttributes


## -description



Gets or sets the drawing attributes for ink that is yet to be drawn on the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.



This property is read/write.


## -parameters


## -remarks



The <b>DrawingAttributes</b> property specifies the appearance of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object. For example, you can specify the width and color of ink drawn on the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

Successive calls to the <b>DrawingAttributes</b> property change only the <b>DrawingAttributes</b> properties of new <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> objects. The calls do not apply to <b>IInkStrokeDisp</b> objects that the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control already collected or is in the process of collecting.

This property is different from the <a href="https://msdn.microsoft.com/de8b2473-092d-4ff9-adbc-3ba378b035e2">DrawingAttributes</a> property of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object, which specifies the attributes of already collected ink. The <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control's <b>DrawingAttributes</b> property is more analogous to the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> object's <a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes</a> property, except that for the <b>DefaultDrawingAttributes</b> property the <a href="https://msdn.microsoft.com/93b11903-84dd-4f7a-a47c-555d19fede8d">FitToCurve</a> property is set to <b>TRUE</b> by default.




## -see-also




<a href="https://msdn.microsoft.com/8F47529B-52E9-4D67-81B3-DD2584B98101">IInkEdit</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

