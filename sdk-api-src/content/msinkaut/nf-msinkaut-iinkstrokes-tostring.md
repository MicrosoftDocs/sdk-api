---
UID: NF:msinkaut.IInkStrokes.ToString
title: IInkStrokes::ToString (msinkaut.h)
description: ToString is no longer available for use as of Windows Vista.
helpviewer_keywords: ["702ec977-2d87-4d52-916e-423f1df03829","IInkStrokes interface [Tablet PC]","ToString method","IInkStrokes.ToString","IInkStrokes::ToString","ToString","ToString method [Tablet PC]","ToString method [Tablet PC]","IInkStrokes interface","msinkaut/IInkStrokes::ToString","tablet.inkstrokes_tostring"]
old-location: tablet\inkstrokes_tostring.htm
tech.root: tablet
ms.assetid: e1f1d68b-16c2-4d97-ae5f-091e5ec285c2
ms.date: 12/05/2018
ms.keywords: 702ec977-2d87-4d52-916e-423f1df03829, IInkStrokes interface [Tablet PC],ToString method, IInkStrokes.ToString, IInkStrokes::ToString, ToString, ToString method [Tablet PC], ToString method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::ToString, tablet.inkstrokes_tostring
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
 - IInkStrokes::ToString
 - msinkaut/IInkStrokes::ToString
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
 - IInkStrokes.ToString
---

# IInkStrokes::ToString


## -description

<p class="CCE_Message">[<b>ToString</b> is no longer available for use as of Windows Vista. Instead, see the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_string">String</a> property for the equivalent of this method for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate</a> object.
]

Has the default recognizer perform recognition on the collection of strokes and returns the top string of the top alternate of the recognition result.

## -parameters

### -param ToString [out, retval]

The top string of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate</a> property of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> object, after the default recognizer performs recognition on the collection of strokes.

For more information about the <b>BSTR</b> data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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
Operation failed.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.
              

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
No recognizers are installed, the recognizers registry key is corrupted, or your environment does not support handwriting recognition.
              

</td>
</tr>
</table>

## -remarks

<b>ToString</b> should not be used for handwriting recognition applications; it can be used for debugging purposes.

<b>ToString</b> returns <b>NULL</b> if:

<ul>
<li>The <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection is empty.</li>
<li>A default recognizer cannot be created.</li>
<li>The default recognizer does not support free input.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkstrokes.md">IInkStrokes</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
