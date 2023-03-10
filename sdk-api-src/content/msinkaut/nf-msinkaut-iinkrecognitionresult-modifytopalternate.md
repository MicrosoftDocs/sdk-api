---
UID: NF:msinkaut.IInkRecognitionResult.ModifyTopAlternate
title: IInkRecognitionResult::ModifyTopAlternate (msinkaut.h)
description: Changes the top alternate of a recognition result by using the specified alternate.
helpviewer_keywords: ["98edc5e9-2388-4f4e-a67f-029ee83be4cb","IInkRecognitionResult interface [Tablet PC]","ModifyTopAlternate method","IInkRecognitionResult.ModifyTopAlternate","IInkRecognitionResult::ModifyTopAlternate","ModifyTopAlternate","ModifyTopAlternate method [Tablet PC]","ModifyTopAlternate method [Tablet PC]","IInkRecognitionResult interface","msinkaut/IInkRecognitionResult::ModifyTopAlternate","tablet.iinkrecognitionresult_modifytopalternate"]
old-location: tablet\iinkrecognitionresult_modifytopalternate.htm
tech.root: tablet
ms.assetid: 98edc5e9-2388-4f4e-a67f-029ee83be4cb
ms.date: 12/05/2018
ms.keywords: 98edc5e9-2388-4f4e-a67f-029ee83be4cb, IInkRecognitionResult interface [Tablet PC],ModifyTopAlternate method, IInkRecognitionResult.ModifyTopAlternate, IInkRecognitionResult::ModifyTopAlternate, ModifyTopAlternate, ModifyTopAlternate method [Tablet PC], ModifyTopAlternate method [Tablet PC],IInkRecognitionResult interface, msinkaut/IInkRecognitionResult::ModifyTopAlternate, tablet.iinkrecognitionresult_modifytopalternate
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
 - IInkRecognitionResult::ModifyTopAlternate
 - msinkaut/IInkRecognitionResult::ModifyTopAlternate
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
 - IInkRecognitionResult.ModifyTopAlternate
---

# IInkRecognitionResult::ModifyTopAlternate


## -description

Changes the top alternate of a recognition result by using the specified alternate.

## -parameters

### -param Alternate [in]

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> to use to modify the top alternate.

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

To retrieve the alternates that can be used to modify the recognition result, call the <a href="/previous-versions/windows/desktop/legacy/ms698186(v=vs.85)">AlternatesFromSelection</a> method.

<div class="alert"><b>Note</b>  A call to <b>ModifyTopAlternate Method</b> may modify the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring">TopString</a> and <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate</a> properties.</div>
<div> </div>
The alternate used in the function can be a word alternate in an entire sentence. For example, an alternate obtained by using <a href="/previous-versions/windows/desktop/legacy/ms698186(v=vs.85)">AlternatesFromSelection</a> (0, 5) for "Hello World" only changes the "Hello" part of the word leaving the "World" part intact.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms698186(v=vs.85)">GetAlternatesFromSelection Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring">TopString Property</a>