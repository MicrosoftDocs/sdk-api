---
UID: NF:msinkaut.IInkRecognizerContext.StopBackgroundRecognition
title: IInkRecognizerContext::StopBackgroundRecognition
author: windows-sdk-content
description: Ends background recognition that was started with a call to BackgroundRecognize or BackgroundRecognizeWithAlternates.
old-location: tablet\inkrecognizercontext_stopbackgroundrecognition.htm
tech.root: tablet
ms.assetid: 25ece9a1-cbc3-43ae-85ec-e3bf78a4e5a0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 25ece9a1-cbc3-43ae-85ec-e3bf78a4e5a0, IInkRecognizerContext, IInkRecognizerContext interface [Tablet PC],StopBackgroundRecognition method, IInkRecognizerContext.StopBackgroundRecognition, IInkRecognizerContext::StopBackgroundRecognition, StopBackgroundRecognition, StopBackgroundRecognition method [Tablet PC], StopBackgroundRecognition method [Tablet PC],IInkRecognizerContext interface, msinkaut/IInkRecognizerContext::StopBackgroundRecognition, tablet.inkrecognizercontext_stopbackgroundrecognition
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
 - IInkRecognizerContext.StopBackgroundRecognition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/D3DC08E9-19CC-4281-9C71-CB9B8CBDDB7F">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

