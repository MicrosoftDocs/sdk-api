---
UID: NF:msinkaut.IInkRecognitionAlternate.AlternatesWithConstantPropertyValues
title: IInkRecognitionAlternate::AlternatesWithConstantPropertyValues
author: windows-sdk-content
description: Retrieves a IInkRecognitionAlternates collection, which are a division of the IInkRecognitionAlternate object on which this method is called.
old-location: tablet\iinkrecognitionalternate_alternateswithconstantpropertyvalues.htm
old-project: tablet
ms.assetid: 6c199960-e0ee-4370-a302-a45a3dbe8b28
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: 6c199960-e0ee-4370-a302-a45a3dbe8b28, AlternatesWithConstantPropertyValues, AlternatesWithConstantPropertyValues method [Tablet PC], AlternatesWithConstantPropertyValues method [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],AlternatesWithConstantPropertyValues method, IInkRecognitionAlternate.AlternatesWithConstantPropertyValues, IInkRecognitionAlternate::AlternatesWithConstantPropertyValues, msinkaut/IInkRecognitionAlternate::AlternatesWithConstantPropertyValues, tablet.iinkrecognitionalternate_alternateswithconstantpropertyvalues
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionAlternate.AlternatesWithConstantPropertyValues
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionAlternate::AlternatesWithConstantPropertyValues


## -description



Retrieves a <a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates</a> collection, which are a division of the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object on which this method is called.




## -parameters




### -param PropertyType




### -param AlternatesWithConstantPropertyValues [out, retval]

When this method returns, contains an <a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates</a> collection which is made up of a division of the alternate on which this method is called. Each <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object in the collection contains adjacent recognition segments which have the same property value for the <i>propertyType</i> parameter.


#### - propertyType [in]

Specifies a string value that identifies the property. For a list of the properties that can be used, see <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty</a>.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
<li>
              Recognition segment boundaries.</li>
</ul>
For a complete list of property types, see <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty</a>.

<div class="alert"><b>Note</b>  The recognizer determines the segmentation of strokes into the recognition segments. Some recognition segments, such as spaces, may correspond to an empty <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.</div>
<div> </div>
<div class="alert"><b>Note</b>  The recognizer determines the ordering of the recognition segments. Therefore, adjacent recognition segments may be based on the order in which the ink was drawn or based on location, such as whether it is positioned left-to-right, positioned top-to-bottom, and so on.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/ef3ab614-7aff-4660-bb2a-783f14e75b94">ConfidenceAlternates</a> property is an alternative to the <b>AlternatesWithConstantPropertyValues</b> method, where <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">ConfidenceLevel</a> is the RecognitionProperty that separates the alternates in the returned recognition alternates collection.

The <a href="https://msdn.microsoft.com/ccdf3092-b0a0-4626-b614-164548b1ca72">LineAlternates</a> property is an alternative to the <b>AlternatesWithConstantPropertyValues</b> method, where <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">LineNumber</a> is the RecognitionProperty that separates the alternates in the returned recognition alternates collection.

<div class="alert"><b>Note</b>  The <b>AlternatesWithConstantPropertyValues</b> method, the <a href="https://msdn.microsoft.com/ccdf3092-b0a0-4626-b614-164548b1ca72">LineAlternates</a> property, and the <a href="https://msdn.microsoft.com/ef3ab614-7aff-4660-bb2a-783f14e75b94">ConfidenceAlternates</a> property of the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object function differently than the <a href="https://msdn.microsoft.com/506b36bc-390c-42ef-9a5e-8f15129d47f8">AlternatesFromSelection</a> method of the <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult</a> object. <b>AlternatesFromSelection</b> returns a collection of alternates for the requested segments of the recognition result.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ef3ab614-7aff-4660-bb2a-783f14e75b94">ConfidenceAlternates Property</a>



<a href="https://msdn.microsoft.com/506b36bc-390c-42ef-9a5e-8f15129d47f8">GetAlternatesFromSelection Method</a>



<a href="https://msdn.microsoft.com/b2ebf45a-b995-4fbc-b86d-b94d1f48f659">GetPropertyValue Method</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates Interface</a>



<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/ccdf3092-b0a0-4626-b614-164548b1ca72">LineAlternates Property</a>
 

 

