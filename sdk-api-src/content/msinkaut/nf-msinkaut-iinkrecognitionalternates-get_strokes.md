---
UID: NF:msinkaut.IInkRecognitionAlternates.get_Strokes
title: IInkRecognitionAlternates::get_Strokes (msinkaut.h)
description: Gets the collection of strokes that are contained in an object or used to create an object.
helpviewer_keywords: ["IInkRecognitionAlternates interface [Tablet PC]","Strokes property","IInkRecognitionAlternates.Strokes","IInkRecognitionAlternates.get_Strokes","IInkRecognitionAlternates::Strokes","IInkRecognitionAlternates::get_Strokes","Strokes property [Tablet PC]","Strokes property [Tablet PC]","IInkRecognitionAlternates interface","get_Strokes","msinkaut/IInkRecognitionAlternates::Strokes","msinkaut/IInkRecognitionAlternates::get_Strokes","tablet.iinkrecognitionalternates_strokes"]
old-location: tablet\iinkrecognitionalternates_strokes.htm
tech.root: tablet
ms.assetid: ce483ea1-4b66-4a87-89a7-f71feae8ccc4
ms.date: 12/05/2018
ms.keywords: IInkRecognitionAlternates interface [Tablet PC],Strokes property, IInkRecognitionAlternates.Strokes, IInkRecognitionAlternates.get_Strokes, IInkRecognitionAlternates::Strokes, IInkRecognitionAlternates::get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkRecognitionAlternates interface, get_Strokes, msinkaut/IInkRecognitionAlternates::Strokes, msinkaut/IInkRecognitionAlternates::get_Strokes, tablet.iinkrecognitionalternates_strokes
f1_keywords:
- msinkaut/IInkRecognitionAlternates.Strokes
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
- IInkRecognitionAlternates.Strokes
- IInkRecognitionAlternates.get_Strokes
- IInkRecognitionAlternates.get_Strokes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognitionAlternates::get_Strokes


## -description



Gets the collection of strokes that are contained in an object or used to create an object.



This property is read-only.


## -parameters


## -remarks



The collection of strokes may be the copies of the strokes contained in an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object or the strokes that were used to create the object or collection.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes</a> property for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object does not return the actual collection that the <b>InkDisp</b> object works with, but instead returns a copy. For example, this means that adding or removing strokes to this collection does not affect the <b>InkDisp</b> object's strokes; to add or remove strokes, use <b>InkDisp</b> methods such as <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle">AddStrokesAtRectangle</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke">DeleteStroke</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a>. However, each stroke in the collection is a reference to the original <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
 

 

