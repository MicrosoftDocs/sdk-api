---
UID: NF:msinkaut.IInkRecognizerContext.Recognize
title: IInkRecognizerContext::Recognize
author: windows-sdk-content
description: Performs recognition on an InkStrokes collection and returns recognition results.
old-location: tablet\inkrecognizercontext_recognize.htm
tech.root: tablet
ms.assetid: 83695dfd-3634-47e7-8311-7216876a827a
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 83695dfd-3634-47e7-8311-7216876a827a, IInkRecognizerContext interface [Tablet PC],Recognize method, IInkRecognizerContext.Recognize, IInkRecognizerContext::Recognize, Recognize, Recognize method [Tablet PC], Recognize method [Tablet PC],IInkRecognizerContext interface, msinkaut/IInkRecognizerContext::Recognize, tablet.inkrecognizercontext_recognize
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
 - IInkRecognizerContext.Recognize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext::Recognize


## -description



Performs recognition on an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection and returns recognition results.




## -parameters




### -param RecognitionStatus [in, out]

The most recent <a href="https://msdn.microsoft.com/d6ff29a8-d100-4bfe-848b-941367d8b2dd">InkRecognitionStatus</a> value.


### -param RecognitionResult [out, retval]

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult</a> results of a recognized collection of strokes, or else <b>NULL</b> if the recognizer could not compute a result for the ink.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
</table>
 




## -remarks



This method performs recognition synchronously. To start background or asynchronous recognition, call the <a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a> or <a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates</a> methods.

You must use a try/catch block when calling <b>Recognize</b> because an exception is thrown when the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object contains no strokes or only deleted strokes.




## -see-also




<a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize Method</a>



<a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates Method</a>



<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/D3DC08E9-19CC-4281-9C71-CB9B8CBDDB7F">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

