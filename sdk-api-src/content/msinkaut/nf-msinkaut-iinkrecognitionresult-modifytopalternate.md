---
UID: NF:msinkaut.IInkRecognitionResult.ModifyTopAlternate
title: IInkRecognitionResult::ModifyTopAlternate method
author: windows-driver-content
description: Changes the top alternate of a recognition result by using the specified alternate.
old-location: tablet\iinkrecognitionresult_modifytopalternate.htm
old-project: tablet
ms.assetid: 98edc5e9-2388-4f4e-a67f-029ee83be4cb
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 98edc5e9-2388-4f4e-a67f-029ee83be4cb, IInkRecognitionResult, IInkRecognitionResult interface [Tablet PC], ModifyTopAlternate method, IInkRecognitionResult::ModifyTopAlternate, ModifyTopAlternate method [Tablet PC], ModifyTopAlternate method [Tablet PC], IInkRecognitionResult interface, ModifyTopAlternate,IInkRecognitionResult.ModifyTopAlternate, msinkaut/IInkRecognitionResult::ModifyTopAlternate, tablet.iinkrecognitionresult_modifytopalternate
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
-	IInkRecognitionResult.ModifyTopAlternate
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkRecognitionResult::ModifyTopAlternate method


## -description



Changes the top alternate of a recognition result by using the specified alternate.




## -parameters




### -param Alternate






#### - alternate [in]

The <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> to use to modify the top alternate.


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
<dt><b>TPC_E_NOT_RELEVANT</b></dt>
</dl>
</td>
<td width="60%">
The lattice does not contain data.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The alternate does not match the known range, or it was not obtained from this lattice.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



By default, the best result string of the recognition result corresponds to the <b>top alternate</b>. However, you can use this method to specify that alternates other than the top alternate are used in the result. When you choose an alternate other than the top alternate, you are essentially choosing a different path through the lattice of alternates that are associated with the results.

To retrieve the alternates that can be used to modify the recognition result, call the <a href="https://msdn.microsoft.com/506b36bc-390c-42ef-9a5e-8f15129d47f8">AlternatesFromSelection</a> method.

<div class="alert"><b>Note</b>  A call to <b>ModifyTopAlternate Method</b> may modify the <a href="https://msdn.microsoft.com/9f345372-0208-4c78-9da7-9b334c0f281e">TopString</a> and <a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a> properties.</div>
<div> </div>
The alternate used in the function can be a word alternate in an entire sentence. For example, an alternate obtained by using <a href="https://msdn.microsoft.com/506b36bc-390c-42ef-9a5e-8f15129d47f8">AlternatesFromSelection</a> (0, 5) for "Hello World" only changes the "Hello" part of the word leaving the "World" part intact.




## -see-also




<a href="https://msdn.microsoft.com/506b36bc-390c-42ef-9a5e-8f15129d47f8">GetAlternatesFromSelection Method</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate Property</a>



<a href="https://msdn.microsoft.com/9f345372-0208-4c78-9da7-9b334c0f281e">TopString Property</a>
 

 

