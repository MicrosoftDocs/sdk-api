---
UID: NF:msinkaut.IInkStrokes.RemoveRecognitionResult
title: IInkStrokes::RemoveRecognitionResult (msinkaut.h)
description: Removes the RecognitionResult that is associated with the InkStrokes collection.
helpviewer_keywords: ["1a1a2027-e0b7-40c5-b396-b6b4039d6b5b","IInkStrokes interface [Tablet PC]","RemoveRecognitionResult method","IInkStrokes.RemoveRecognitionResult","IInkStrokes::RemoveRecognitionResult","RemoveRecognitionResult","RemoveRecognitionResult method [Tablet PC]","RemoveRecognitionResult method [Tablet PC]","IInkStrokes interface","msinkaut/IInkStrokes::RemoveRecognitionResult","tablet.inkstrokes_removerecognitionresult"]
old-location: tablet\inkstrokes_removerecognitionresult.htm
tech.root: tablet
ms.assetid: 1a1a2027-e0b7-40c5-b396-b6b4039d6b5b
ms.date: 12/05/2018
ms.keywords: 1a1a2027-e0b7-40c5-b396-b6b4039d6b5b, IInkStrokes interface [Tablet PC],RemoveRecognitionResult method, IInkStrokes.RemoveRecognitionResult, IInkStrokes::RemoveRecognitionResult, RemoveRecognitionResult, RemoveRecognitionResult method [Tablet PC], RemoveRecognitionResult method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::RemoveRecognitionResult, tablet.inkstrokes_removerecognitionresult
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokes::RemoveRecognitionResult
 - msinkaut/IInkStrokes::RemoveRecognitionResult
dev_langs:
 - c++
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
---

# IInkStrokes::RemoveRecognitionResult


## -description

Removes the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-get_recognitionresult">RecognitionResult</a> that is associated with the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection.



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

To set a recognition result on an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection, use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-setresultonstrokes">SetResultOnStrokes</a> method.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
