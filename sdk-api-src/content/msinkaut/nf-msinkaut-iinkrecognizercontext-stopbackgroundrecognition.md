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

# IInkRecognizerContext::StopBackgroundRecognition


## -description



Ends background recognition that was started with a call to <a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a> or <a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates</a>.




## -parameters






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

This method also returns S_OK if the recognizer does not support this method.

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
An exception occurred inside method.

</td>
</tr>
</table>
 




## -remarks



No event is fired if <b>StopBackgroundRecognition</b> is called.

Call <b>StopBackgroundRecognition</b> if you call <a href="https://msdn.microsoft.com/d3fc8117-4acd-474a-aec0-cb421230ef94">BackgroundRecognize</a> or <a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates</a> one or more times. Calling <b>StopBackgroundRecognition</b> does not necessarily ensure that you get no results from a recognition process that is currently under way. It only ensures that all previous calls to <b>BackgroundRecognize</b> or <b>BackgroundRecognizeWithAlternates</b> that have not yet been processed are actually not executed.

Call this method only if you process the ink asynchronously.




## -see-also




<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

