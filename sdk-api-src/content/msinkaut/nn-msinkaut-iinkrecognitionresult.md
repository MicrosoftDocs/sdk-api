---
UID: NN:msinkaut.IInkRecognitionResult
title: IInkRecognitionResult
author: windows-sdk-content
description: Represents the result of the recognition. The results of recognizing handwritten ink are returned in an IInkRecognitionResult object.
old-location: tablet\iinkrecognitionresult.htm
old-project: tablet
ms.assetid: fd7ee250-6f76-419b-8164-0d2717ea288c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInkRecognitionResult, IInkRecognitionResult interface [Tablet PC], IInkRecognitionResult interface [Tablet PC],described, fd7ee250-6f76-419b-8164-0d2717ea288c, msinkaut/IInkRecognitionResult, tablet.iinkrecognitionresult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
 - IInkRecognitionResult
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionResult interface


## -description



Represents the result of the recognition. The results of recognizing handwritten ink are returned in an <b>IInkRecognitionResult</b> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRecognitionResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkRecognitionResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/506b36bc-390c-42ef-9a5e-8f15129d47f8">GetAlternatesFromSelection</a>
</td>
<td align="left" width="63%">
Retrieves the alternate collection from a selection within the best result string of the recognition result so that each alternate corresponds to only one segment of ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate Method</a>
</td>
<td align="left" width="63%">
Modifies the recognition result with a known alternate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/928f6f39-1b8f-403a-8c18-0931c5a6dc5d">SetResultOnStrokes</a>
</td>
<td align="left" width="63%">
Assigns the recognition results to the strokes that were used to create the results.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRecognitionResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/57659ad8-b1ca-4da0-94fb-4807a6f9af2f">Strokes</a>


</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> that was used by the recognizer to generate the <b>IInkRecognitionResult</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a>


</td>
<td align="left" width="63%">
Gets the top alternate of the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/286283ca-a8ad-4fc5-ae46-09a3e6382e2a">TopConfidence</a>


</td>
<td align="left" width="63%">
Gets the confidence level of the <a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a> property of the <b>IInkRecognitionResult</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f345372-0208-4c78-9da7-9b334c0f281e">TopString</a>


</td>
<td align="left" width="63%">
Gets the result text for the <a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a> property.

</td>
</tr>
</table> 


## -remarks




<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> objects, or alternates, are created from the result. The best, or top, alternate is the one that is used by the default in the result. However, you can use the methods of the <b>IInkRecognitionResult</b> object to specify which alternates to use in the result.

System performance can suffer if recognition results are automatically assigned to every collection of stroke. Therefore, by default, results are not attached to a collection of strokes. You must call the <a href="https://msdn.microsoft.com/928f6f39-1b8f-403a-8c18-0931c5a6dc5d">SetResultOnStrokes</a> method to assign results to a collection of strokes.

The only way to persist recognition results is to call <a href="https://msdn.microsoft.com/928f6f39-1b8f-403a-8c18-0931c5a6dc5d">SetResultOnStrokes</a> and then add this collection of strokes to the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">CustomStrokes</a> collection on the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

Not all recognizers set the <a href="https://msdn.microsoft.com/286283ca-a8ad-4fc5-ae46-09a3e6382e2a">TopConfidence</a> property. When an application attempts to access a property that is not set by the recognizer, an argument exception is thrown.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

<div class="alert"><b>Note</b>  The various handwriting recognizers shipped from Microsoft in both Latin characters  and East Asian languages can sometimes produce the Unicode value 0xFFFF as the recognition result. This occurs when the recognizer is unable to match a piece of ink with any valid character. The 0xFFFF code point is valid UCS-2, but not allowed in UTF-8. An application that converts recognition results to UTF-8, should replace 0xFFFF with some other code point, for example, 0xFFFD.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33425e5b-2ba0-4026-ab19-33579e7bb9f5">CustomStrokes Property [InkDisp Class]</a>



<a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes Interface</a>



<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

