---
UID: NF:msinkaut.IInkDrawingAttributes.put_FitToCurve
title: IInkDrawingAttributes::put_FitToCurve (msinkaut.h)
description: Gets or sets the value that specifies whether Bezier smoothing is used to render ink.helpviewer_keywords: ["93b11903-84dd-4f7a-a47c-555d19fede8d","FitToCurve property [Tablet PC]","FitToCurve property [Tablet PC]","IInkDrawingAttributes interface","IInkDrawingAttributes interface [Tablet PC]","FitToCurve property","IInkDrawingAttributes.FitToCurve","IInkDrawingAttributes.put_FitToCurve","IInkDrawingAttributes::FitToCurve","IInkDrawingAttributes::get_FitToCurve","IInkDrawingAttributes::put_FitToCurve","InkDrawingAttributes.get_FitToCurve","InkDrawingAttributes.put_FitToCurve","msinkaut/IInkDrawingAttributes::FitToCurve","msinkaut/IInkDrawingAttributes::get_FitToCurve","msinkaut/IInkDrawingAttributes::put_FitToCurve","put_FitToCurve","tablet.inkdrawingattributes_fittocurve"]
old-location: tablet\inkdrawingattributes_fittocurve.htm
tech.root: tablet
ms.assetid: 93b11903-84dd-4f7a-a47c-555d19fede8d
ms.date: 12/05/2018
ms.keywords: 93b11903-84dd-4f7a-a47c-555d19fede8d, FitToCurve property [Tablet PC], FitToCurve property [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],FitToCurve property, IInkDrawingAttributes.FitToCurve, IInkDrawingAttributes.put_FitToCurve, IInkDrawingAttributes::FitToCurve, IInkDrawingAttributes::get_FitToCurve, IInkDrawingAttributes::put_FitToCurve, InkDrawingAttributes.get_FitToCurve, InkDrawingAttributes.put_FitToCurve, msinkaut/IInkDrawingAttributes::FitToCurve, msinkaut/IInkDrawingAttributes::get_FitToCurve, msinkaut/IInkDrawingAttributes::put_FitToCurve, put_FitToCurve, tablet.inkdrawingattributes_fittocurve
f1_keywords:
- msinkaut/IInkDrawingAttributes.FitToCurve
dev_langs:
- c++
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkDrawingAttributes.FitToCurve
- IInkDrawingAttributes.get_FitToCurve
- IInkDrawingAttributes.put_FitToCurve
- InkDrawingAttributes.get_FitToCurve
- InkDrawingAttributes.put_FitToCurve
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDrawingAttributes::put_FitToCurve


## -description



Gets or sets the value that specifies whether Bezier smoothing is used to render ink.



This property is read/write.


## -parameters


## -remarks



Bezier smoothing renders ink as a series of curves instead of as lines between pen sample points. Rendering ink as a series of curves is useful for smoothing the ink, especially when the person writing the ink has unsteady writing.

If you set this property while collecting a stroke or strokes, the ink does not render as a series of curves until it is redrawn or refreshed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getflattenedbezierpoints">GetFlattenedBezierPoints Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846798(v=VS.85).aspx">IInkDrawingAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>
 

 

