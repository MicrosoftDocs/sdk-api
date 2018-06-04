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

# IInkRecognizerContext::EndInkInput


## -description


<p class="CCE_Message">[<b>EndInkInput</b> is no longer available for use for recognizers of western languages as of Windows Vista.]

Stops adding ink to the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">

                An exception occurred inside the method.
              

</td>
</tr>
</table>
 




## -remarks



After you call this method, you cannot add strokes to the context.

This method deals with partial recognition. Partial recognition is the ability of the recognizer to return results even if the application has not called <b>EndInkInput</b> (which signals to the application that all the ink has been entered). Partial recognition occurs only if the recognizer can determine that ink has been entered before a call to <b>EndInkInput</b>, and not all recognizers support this feature. Recognizers that do not support partial recognition do not return any result until <b>EndInkInput</b> is called. Calling for <b>EndInkInput</b> is optional.

Incremental recognition is the ability of the recognizer to process only a small part of the ink that has been passed to it and return a result. For example, consider that an application contains five lines of ink and uses a recognizer of Latin script. The recognizer can process only one line at a time and return a result. This process is used in the idle loop of the background processing thread.




## -see-also




<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

