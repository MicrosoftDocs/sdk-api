---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Strokes
title: IInkRecognitionAlternate::get_Strokes (msinkaut.h)
description: Gets the collection of strokes that are contained in an object or used to create an object. (IInkRecognitionAlternate.get_Strokes)
helpviewer_keywords: ["IInkRecognitionAlternate interface [Tablet PC]","Strokes property","IInkRecognitionAlternate.Strokes","IInkRecognitionAlternate.get_Strokes","IInkRecognitionAlternate::Strokes","IInkRecognitionAlternate::get_Strokes","Strokes property [Tablet PC]","Strokes property [Tablet PC]","IInkRecognitionAlternate interface","get_Strokes","msinkaut/IInkRecognitionAlternate::Strokes","msinkaut/IInkRecognitionAlternate::get_Strokes","tablet.iinkrecognitionalternate_strokes"]
old-location: tablet\iinkrecognitionalternate_strokes.htm
tech.root: tablet
ms.assetid: 60ce6ed5-67d3-4471-a7a1-4653e8a122a1
ms.date: 12/05/2018
ms.keywords: IInkRecognitionAlternate interface [Tablet PC],Strokes property, IInkRecognitionAlternate.Strokes, IInkRecognitionAlternate.get_Strokes, IInkRecognitionAlternate::Strokes, IInkRecognitionAlternate::get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkRecognitionAlternate interface, get_Strokes, msinkaut/IInkRecognitionAlternate::Strokes, msinkaut/IInkRecognitionAlternate::get_Strokes, tablet.iinkrecognitionalternate_strokes
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
 - IInkRecognitionAlternate::get_Strokes
 - msinkaut/IInkRecognitionAlternate::get_Strokes
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
 - IInkRecognitionAlternate.Strokes
 - IInkRecognitionAlternate.get_Strokes
 - IInkRecognitionAlternate.get_Strokes
---

# IInkRecognitionAlternate::get_Strokes


## -description

Gets the collection of strokes that are contained in an object or used to create an object.



This property is read-only.

## -parameters

## -remarks

The collection of strokes may be the copies of the strokes contained in an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object or the strokes that were used to create the object or collection.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes</a> property for the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object does not return the actual collection that the <b>InkDisp</b> object works with, but instead returns a copy. For example, this means that adding or removing strokes to this collection does not affect the <b>InkDisp</b> object's strokes; to add or remove strokes, use <b>InkDisp</b> methods such as <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle">AddStrokesAtRectangle</a>, <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke">DeleteStroke</a>, and <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a>. However, each stroke in the collection is a reference to the original <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
