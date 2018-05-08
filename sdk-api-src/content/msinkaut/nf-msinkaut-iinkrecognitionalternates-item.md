---
UID: NF:msinkaut.IInkRecognitionAlternates.Item
title: IInkRecognitionAlternates::Item
author: windows-driver-content
description: Retrieves the IInkRecognitionAlternate object at the specified index within the IInkRecognitionAlternates collection.
old-location: tablet\iinkrecognitionalternates_item.htm
old-project: tablet
ms.assetid: 63a00f6d-f733-4b25-bfe2-4f841b9694fa
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: 63a00f6d-f733-4b25-bfe2-4f841b9694fa, IInkRecognitionAlternates interface [Tablet PC],Item method, IInkRecognitionAlternates.Item, IInkRecognitionAlternates::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkRecognitionAlternates interface, msinkaut/IInkRecognitionAlternates::Item, tablet.iinkrecognitionalternates_item
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
-	IInkRecognitionAlternates.Item
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkRecognitionAlternates::Item


## -description



Retrieves the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object at the specified index within the <a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates</a> collection.




## -parameters




### -param Index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object to get.


### -param InkRecoAlternate [out, retval]

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object at the specified index within the <a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates</a> collection.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not a valid VARIANT type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
Type object not registered.

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
<dt><b>TPC_E_RECOGNIZER_NOT_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The recognizers registry key is corrupted or your environment does not support handwriting recognition.




</td>
</tr>
</table>
 




## -remarks



An error occurs if the index doesn't match any existing member of the collection.




## -see-also




<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/39f49762-de86-4a1a-ac7b-327b65c3eb54">IInkRecognitionAlternates Interface</a>
 

 

