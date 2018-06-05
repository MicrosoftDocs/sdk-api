---
UID: NF:msinkaut.IInkRecognitionResult.get_Strokes
title: IInkRecognitionResult::get_Strokes
author: windows-sdk-content
description: Gets the collection of strokes that are contained in an object or used to create an object.
old-location: tablet\iinkrecognitionresult_strokes.htm
old-project: tablet
ms.assetid: 57659ad8-b1ca-4da0-94fb-4807a6f9af2f
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IInkRecognitionResult interface [Tablet PC],Strokes property, IInkRecognitionResult.Strokes, IInkRecognitionResult.get_Strokes, IInkRecognitionResult::Strokes, IInkRecognitionResult::get_Strokes, Strokes property [Tablet PC], Strokes property [Tablet PC],IInkRecognitionResult interface, get_Strokes, msinkaut/IInkRecognitionResult::Strokes, msinkaut/IInkRecognitionResult::get_Strokes, tablet.iinkrecognitionresult_strokes
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkRecognitionResult.Strokes
-	IInkRecognitionResult.get_Strokes
-	IInkRecognitionResult.get_Strokes
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionResult::get_Strokes


## -description



Gets the collection of strokes that are contained in an object or used to create an object.



This property is read-only.


## -parameters


## -remarks



The collection of strokes may be the copies of the strokes contained in an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object or the strokes that were used to create the object or collection.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/b65f1b71-b0a4-4de2-9321-f660bcd2d3ce">Strokes</a> property for the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object does not return the actual collection that the <b>InkDisp</b> object works with, but instead returns a copy. For example, this means that adding or removing strokes to this collection does not affect the <b>InkDisp</b> object's strokes; to add or remove strokes, use <b>InkDisp</b> methods such as <a href="https://msdn.microsoft.com/c5a7cbbc-361c-4e99-af31-f7114eb5261b">AddStrokesAtRectangle</a>, <a href="https://msdn.microsoft.com/ac6579ec-20f7-4a20-8cb8-5f3a6119959d">DeleteStroke</a>, and <a href="https://msdn.microsoft.com/cbc11006-a434-46f8-a78c-3b67e35ed32a">DeleteStrokes</a>. However, each stroke in the collection is a reference to the original <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

