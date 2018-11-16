---
UID: NF:msinkaut.IInkRecognitionAlternate.GetStrokesFromStrokeRanges
title: IInkRecognitionAlternate::GetStrokesFromStrokeRanges
author: windows-sdk-content
description: Retrieves the smallest InkStrokes collection that contains a known input InkStrokes collection and for which the IInkRecognizer object can provide alternates.
old-location: tablet\iinkrecognitionalternate_getstrokesfromstrokeranges.htm
tech.root: tablet
ms.assetid: 25079651-4fcd-4f13-b73f-7d5ffefa871e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 25079651-4fcd-4f13-b73f-7d5ffefa871e, GetStrokesFromStrokeRanges, GetStrokesFromStrokeRanges method [Tablet PC], GetStrokesFromStrokeRanges method [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],GetStrokesFromStrokeRanges method, IInkRecognitionAlternate.GetStrokesFromStrokeRanges, IInkRecognitionAlternate::GetStrokesFromStrokeRanges, msinkaut/IInkRecognitionAlternate::GetStrokesFromStrokeRanges, tablet.iinkrecognitionalternate_getstrokesfromstrokeranges
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
 - IInkRecognitionAlternate.GetStrokesFromStrokeRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkRecognitionAlternate.GetStrokesFromStrokeRanges
: 
---

# IInkRecognitionAlternate::GetStrokesFromStrokeRanges


## -description



Retrieves the smallest <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection that contains a known input InkStrokes collection and for which the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object can provide alternates.




## -parameters




### -param Strokes [in]

The collection of stroke objects to use to find the smallest stroke collection of the recognition result alternate that contains this collection.


### -param GetStrokesFromStrokeRanges [out, retval]

When this method returns, contains a pointer to the smallest collection of strokes that contains a known input collection of strokes and for which the recognizer can provide alternates.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The strokes parameter is associated with a different Ink object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



The returned collection may match the input collection, or it may be larger if the input collection matches only part of the smallest recognition result that includes all of the input strokes.

This method is most useful for single-click word selection. For example, to return the strokes that make up the word you clicked, you can click a stroke, call the <a href="https://msdn.microsoft.com/b87a1bc0-b17b-419b-947e-48746f4903e8">HitTest</a> method of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object to retrieve the stroke that was clicked, and then call <b>GetStrokesFromStrokeRanges</b>.

The stroke ranges are valid until the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object is modified.




## -see-also




<a href="https://msdn.microsoft.com/7dd8fa24-191f-465d-abd2-9a489df0324a">GetStrokesFromTextRange Method</a>



<a href="https://msdn.microsoft.com/b481e356-0a3c-4437-9700-6d8badcb0b0b">GetTextRangeFromStrokes Method</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognition Alternate Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

