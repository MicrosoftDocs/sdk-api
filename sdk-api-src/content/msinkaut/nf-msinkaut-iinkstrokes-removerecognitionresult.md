---
UID: NF:msinkaut.IInkStrokes.RemoveRecognitionResult
title: IInkStrokes::RemoveRecognitionResult
author: windows-sdk-content
description: Removes the RecognitionResult that is associated with the InkStrokes collection.
old-location: tablet\inkstrokes_removerecognitionresult.htm
old-project: tablet
ms.assetid: 1a1a2027-e0b7-40c5-b396-b6b4039d6b5b
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 1a1a2027-e0b7-40c5-b396-b6b4039d6b5b, IInkStrokes interface [Tablet PC],RemoveRecognitionResult method, IInkStrokes.RemoveRecognitionResult, IInkStrokes::RemoveRecognitionResult, RemoveRecognitionResult, RemoveRecognitionResult method [Tablet PC], RemoveRecognitionResult method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::RemoveRecognitionResult, tablet.inkstrokes_removerecognitionresult
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
 - IInkStrokes.RemoveRecognitionResult
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokes::RemoveRecognitionResult


## -description



Removes the <a href="https://msdn.microsoft.com/5d6e7147-b312-4989-8d8f-88cb2221f6f0">RecognitionResult</a> that is associated with the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection.




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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



To set a recognition result on an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection, use the <a href="https://msdn.microsoft.com/928f6f39-1b8f-403a-8c18-0931c5a6dc5d">SetResultOnStrokes</a> method.




## -see-also




<a href="tablet.iinkstrokes">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

