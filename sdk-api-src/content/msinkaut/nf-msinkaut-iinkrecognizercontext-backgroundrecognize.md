---
UID: NF:msinkaut.IInkRecognizerContext.BackgroundRecognize
title: IInkRecognizerContext::BackgroundRecognize
author: windows-sdk-content
description: Causes the IInkRecognizer object to recognize the associated strokes collection and fire a Recognition event when recognition is complete.
old-location: tablet\inkrecognizercontext_backgroundrecognize.htm
old-project: tablet
ms.assetid: d3fc8117-4acd-474a-aec0-cb421230ef94
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: BackgroundRecognize, BackgroundRecognize method [Tablet PC], BackgroundRecognize method [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],BackgroundRecognize method, IInkRecognizerContext.BackgroundRecognize, IInkRecognizerContext::BackgroundRecognize, d3fc8117-4acd-474a-aec0-cb421230ef94, msinkaut/IInkRecognizerContext::BackgroundRecognize, tablet.inkrecognizercontext_backgroundrecognize
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
 - IInkRecognizerContext.BackgroundRecognize
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognizerContext::BackgroundRecognize


## -description



Causes the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object to recognize the associated strokes collection and fire a <a href="https://msdn.microsoft.com/0cc319af-cd0b-4089-928b-cae6c86f6f61">Recognition</a> event when recognition is complete.




## -parameters




### -param CustomData






#### - customData [in, optional]

Specifies any application-defined data that is available to the application in the <a href="https://msdn.microsoft.com/0cc319af-cd0b-4089-928b-cae6c86f6f61">Recognition</a> event. This parameter may be a VARIANT of type VT_EMPTY or VT_NULL if no data needs to be passed. The default value is <b>NULL</b>.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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



This method specifies that ink recognition is performed asynchronously. To recognize ink synchronously, call the <a href="https://msdn.microsoft.com/83695dfd-3634-47e7-8311-7216876a827a">Recognize</a> method.

This method recognizes only the best result string. Alternates are not created. To perform recognition that creates a list of available alternates, call the <a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates</a> method.

The <a href="https://msdn.microsoft.com/0cc319af-cd0b-4089-928b-cae6c86f6f61">Recognition</a> event is not raised if the recognizer does not recognize anything.




## -see-also




<a href="https://msdn.microsoft.com/1559678c-c220-4c67-aa0f-566377d95818">BackgroundRecognizeWithAlternates Method</a>



<a href="https://msdn.microsoft.com/cde7772a-9996-4011-ae9d-d43caddfef83">Data Property</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms696371(v=vs.85).aspx">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

