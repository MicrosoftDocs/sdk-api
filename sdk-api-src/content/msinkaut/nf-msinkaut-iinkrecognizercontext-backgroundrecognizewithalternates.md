---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkRecognizerContext::BackgroundRecognizeWithAlternates


## -description



Causes the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="https://msdn.microsoft.com/5e86a4d5-c0a7-4283-81cc-ec3a26f74880">RecognitionWithAlternates</a> event when recognition is complete.




## -parameters




### -param CustomData [in, optional]

Optional. Specifies any application-defined data that is available to the application in the <a href="https://msdn.microsoft.com/5e86a4d5-c0a7-4283-81cc-ec3a26f74880">RecognitionWithAlternates</a> event. This parameter may be a VARIANT of type VT_EMPTY or VT_NULL if no data needs to be passed. The default value is <b>NULL</b>.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>HRESULT Value</th>
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
<dt><b>E_INK_NO_STROKES_TO_RECOGNIZE</b></dt>
</dl>
</td>
<td width="60%">
No strokes exist.

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
</table>
 




## -remarks



This method specifies that ink recognition is performed asynchronously.

To perform recognition that includes only the best result string with no alternates, call the <a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a> method.

The <a href="https://msdn.microsoft.com/5e86a4d5-c0a7-4283-81cc-ec3a26f74880">RecognitionWithAlternates</a> event is not raised if the recognizer does not recognize any alternates.




## -see-also




<a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize Method</a>



<a href="https://msdn.microsoft.com/cde7772a-9996-4011-ae9d-d43caddfef83">Data Property</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

