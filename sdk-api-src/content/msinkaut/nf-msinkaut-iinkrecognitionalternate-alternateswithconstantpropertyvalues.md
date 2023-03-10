---
UID: NF:msinkaut.IInkRecognitionAlternate.AlternatesWithConstantPropertyValues
title: IInkRecognitionAlternate::AlternatesWithConstantPropertyValues (msinkaut.h)
description: Retrieves a IInkRecognitionAlternates collection, which are a division of the IInkRecognitionAlternate object on which this method is called.
helpviewer_keywords: ["6c199960-e0ee-4370-a302-a45a3dbe8b28","AlternatesWithConstantPropertyValues","AlternatesWithConstantPropertyValues method [Tablet PC]","AlternatesWithConstantPropertyValues method [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","AlternatesWithConstantPropertyValues method","IInkRecognitionAlternate.AlternatesWithConstantPropertyValues","IInkRecognitionAlternate::AlternatesWithConstantPropertyValues","msinkaut/IInkRecognitionAlternate::AlternatesWithConstantPropertyValues","tablet.iinkrecognitionalternate_alternateswithconstantpropertyvalues"]
old-location: tablet\iinkrecognitionalternate_alternateswithconstantpropertyvalues.htm
tech.root: tablet
ms.assetid: 6c199960-e0ee-4370-a302-a45a3dbe8b28
ms.date: 12/05/2018
ms.keywords: 6c199960-e0ee-4370-a302-a45a3dbe8b28, AlternatesWithConstantPropertyValues, AlternatesWithConstantPropertyValues method [Tablet PC], AlternatesWithConstantPropertyValues method [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],AlternatesWithConstantPropertyValues method, IInkRecognitionAlternate.AlternatesWithConstantPropertyValues, IInkRecognitionAlternate::AlternatesWithConstantPropertyValues, msinkaut/IInkRecognitionAlternate::AlternatesWithConstantPropertyValues, tablet.iinkrecognitionalternate_alternateswithconstantpropertyvalues
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
 - IInkRecognitionAlternate::AlternatesWithConstantPropertyValues
 - msinkaut/IInkRecognitionAlternate::AlternatesWithConstantPropertyValues
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
 - IInkRecognitionAlternate.AlternatesWithConstantPropertyValues
---

# IInkRecognitionAlternate::AlternatesWithConstantPropertyValues


## -description

Retrieves a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates</a> collection, which are a division of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object on which this method is called.

## -parameters

### -param PropertyType [in]

Specifies a string value that identifies the property. For a list of the properties that can be used, see <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a>.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param AlternatesWithConstantPropertyValues [out, retval]

When this method returns, contains an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates</a> collection which is made up of a division of the alternate on which this method is called. Each <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object in the collection contains adjacent recognition segments which have the same property value for the <i>propertyType</i> parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The recognition range is invalid.

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

Each alternate in the collection contains adjacent recognition segments which have the same property value for the property passed into the method.

For example, you can return alternates that divide the original alternate by:

<ul>
<li>Level of confidence boundaries-strong, intermediate, or poor-in the recognition result.</li>
<li>Line boundaries.</li>
<li>Recognition segment boundaries.</li>
</ul>
For a complete list of property types, see <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a>.

<div class="alert"><b>Note</b>  The recognizer determines the segmentation of strokes into the recognition segments. Some recognition segments, such as spaces, may correspond to an empty <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.</div>
<div> </div>
<div class="alert"><b>Note</b>  The recognizer determines the ordering of the recognition segments. Therefore, adjacent recognition segments may be based on the order in which the ink was drawn or based on location, such as whether it is positioned left-to-right, positioned top-to-bottom, and so on.</div>
<div> </div>
The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates">ConfidenceAlternates</a> property is an alternative to the <b>AlternatesWithConstantPropertyValues</b> method, where <a href="/windows/desktop/tablet/recognitionproperty-constants">ConfidenceLevel</a> is the RecognitionProperty that separates the alternates in the returned recognition alternates collection.

The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a> property is an alternative to the <b>AlternatesWithConstantPropertyValues</b> method, where <a href="/windows/desktop/tablet/recognitionproperty-constants">LineNumber</a> is the RecognitionProperty that separates the alternates in the returned recognition alternates collection.

<div class="alert"><b>Note</b>  The <b>AlternatesWithConstantPropertyValues</b> method, the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates</a> property, and the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates">ConfidenceAlternates</a> property of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object function differently than the <a href="/previous-versions/windows/desktop/legacy/ms698186(v=vs.85)">AlternatesFromSelection</a> method of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> object. <b>AlternatesFromSelection</b> returns a collection of alternates for the requested segments of the recognition result.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates">ConfidenceAlternates Property</a>



<a href="/previous-versions/windows/desktop/legacy/ms698186(v=vs.85)">GetAlternatesFromSelection Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue">GetPropertyValue Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates Property</a>