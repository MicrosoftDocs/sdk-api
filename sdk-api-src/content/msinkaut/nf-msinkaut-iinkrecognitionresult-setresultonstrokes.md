---
UID: NF:msinkaut.IInkRecognitionResult.SetResultOnStrokes
title: IInkRecognitionResult::SetResultOnStrokes (msinkaut.h)
description: Assigns the recognition results to the strokes that were used to create the results.
old-location: tablet\iinkrecognitionresult_setresultonstrokes.htm
tech.root: tablet
ms.assetid: 928f6f39-1b8f-403a-8c18-0931c5a6dc5d
ms.date: 12/05/2018
ms.keywords: 928f6f39-1b8f-403a-8c18-0931c5a6dc5d, IInkRecognitionResult interface [Tablet PC],SetResultOnStrokes method, IInkRecognitionResult.SetResultOnStrokes, IInkRecognitionResult::SetResultOnStrokes, SetResultOnStrokes, SetResultOnStrokes method [Tablet PC], SetResultOnStrokes method [Tablet PC],IInkRecognitionResult interface, msinkaut/IInkRecognitionResult::SetResultOnStrokes, tablet.iinkrecognitionresult_setresultonstrokes
ms.topic: method
f1_keywords:
- msinkaut/IInkRecognitionResult.SetResultOnStrokes
dev_langs:
- c++
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
- IInkRecognitionResult.SetResultOnStrokes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognitionResult::SetResultOnStrokes


## -description



Assigns the recognition results to the strokes that were used to create the results.




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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
</table>
 




## -remarks



System performance suffers if recognition results are automatically assigned to every <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection. Therefore results are not attached to an InkStrokes collection by default. To assign results to an InkStrokes collection, you must call <b>SetResultOnStrokes</b>. To return the recognition results for a InkStrokes collection, use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> property of the InkStrokes collection. After you assign results to a InkStrokes collection, you can then store the strokes in a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection. These custom strokes, as well as the <b>IInkRecognitionResult</b>, can be persisted and retrieved for later use.

To return the recognition results of a collection of strokes, use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-get_recognitionresult">RecognitionResult</a> property.

After you assign results to a collection of strokes, you can then store the strokes in an <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection. These custom strokes, as well as the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a>, can be persisted and retrieved for later use.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-get_recognitionresult">RecognitionResult Property</a>
 

 

