---
UID: NF:msinkaut.IInkRecognizerContext.EndInkInput
title: IInkRecognizerContext::EndInkInput
author: windows-sdk-content
description: EndInkInput is no longer available for use for recognizers of western languages as of Windows Vista.
old-location: tablet\inkrecognizercontext_endinkinput.htm
tech.root: tablet
ms.assetid: a384edf8-3b3d-4e0c-b39c-976798457076
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndInkInput, EndInkInput method [Tablet PC], EndInkInput method [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],EndInkInput method, IInkRecognizerContext.EndInkInput, IInkRecognizerContext::EndInkInput, a384edf8-3b3d-4e0c-b39c-976798457076, msinkaut/IInkRecognizerContext::EndInkInput, tablet.inkrecognizercontext_endinkinput
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
 - IInkRecognizerContext.EndInkInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Mt846801(v=VS.85).aspx">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

