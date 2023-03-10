---
UID: NF:msinkaut.IInkRecognitionResult.get_Strokes
title: IInkRecognitionResult::get_Strokes (msinkaut.h)
description: Gets the collection of strokes that are contained in an object or used to create an object. (IInkRecognitionResult.get_Strokes)
helpviewer_keywords: ["IInkRecognitionResult interface [Tablet PC]","Strokes property","IInkRecognitionResult.Strokes","IInkRecognitionResult.get_Strokes","IInkRecognitionResult::Strokes","IInkRecognitionResult::get_Strokes","Strokes property [Tablet PC]","Strokes property [Tablet PC]","IInkRecognitionResult interface","get_Strokes","msinkaut/IInkRecognitionResult::Strokes","msinkaut/IInkRecognitionResult::get_Strokes","tablet.iinkrecognitionresult_strokes"]
old-location: tablet\iinkrecognitionresult_strokes.htm
tech.root: tablet
ms.assetid: 57659ad8-b1ca-4da0-94fb-4807a6f9af2f
ms.date: 12/05/2018
ms.keywords: IInkRecognitionResult interface [Tablet PC],Strokes property, IInkRecognitionResult.Strokes, IInkRecognitionResult.get_Strokes, IInkRecognitionResult::Strokes, IInkRecognitionResult::get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkRecognitionResult interface, get_Strokes, msinkaut/IInkRecognitionResult::Strokes, msinkaut/IInkRecognitionResult::get_Strokes, tablet.iinkrecognitionresult_strokes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognitionResult::get_Strokes
 - msinkaut/IInkRecognitionResult::get_Strokes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionResult.Strokes
 - IInkRecognitionResult.get_Strokes
 - IInkRecognitionResult.get_Strokes
---

# IInkRecognitionResult::get_Strokes


## -description

Gets the collection of strokes that are contained in an object or used to create an object.



This property is read-only.

## -parameters

## -remarks

The collection of strokes may be the copies of the strokes contained in an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object or the strokes that were used to create the object or collection.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes</a> property for the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object does not return the actual collection that the <b>InkDisp</b> object works with, but instead returns a copy. For example, this means that adding or removing strokes to this collection does not affect the <b>InkDisp</b> object's strokes; to add or remove strokes, use <b>InkDisp</b> methods such as <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle">AddStrokesAtRectangle</a>, <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke">DeleteStroke</a>, and <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a>. However, each stroke in the collection is a reference to the original <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
