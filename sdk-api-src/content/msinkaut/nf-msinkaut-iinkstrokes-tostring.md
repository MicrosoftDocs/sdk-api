---
UID: NF:msinkaut.IInkStrokes.ToString
title: IInkStrokes::ToString
author: windows-sdk-content
description: ToString is no longer available for use as of Windows Vista.
old-location: tablet\inkstrokes_tostring.htm
old-project: tablet
ms.assetid: e1f1d68b-16c2-4d97-ae5f-091e5ec285c2
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 702ec977-2d87-4d52-916e-423f1df03829, IInkStrokes interface [Tablet PC],ToString method, IInkStrokes.ToString, IInkStrokes::ToString, ToString, ToString method [Tablet PC], ToString method [Tablet PC],IInkStrokes interface, msinkaut/IInkStrokes::ToString, tablet.inkstrokes_tostring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
 - IInkStrokes.ToString
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokes::ToString


## -description


<p class="CCE_Message">[<b>ToString</b> is no longer available for use as of Windows Vista. Instead, see the <a href="https://msdn.microsoft.com/1f603794-3b6a-4e8f-9804-fa4c85d82d1c">String</a> property for the equivalent of this method for the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object.
]

Has the default recognizer perform recognition on the collection of strokes and returns the top string of the top alternate of the recognition result.


## -parameters




### -param ToString [out, retval]

The top string of the <a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a> property of the <a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult</a> object, after the default recognizer performs recognition on the collection of strokes.

For more information about the <b>BSTR</b> data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
<li>The <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection is empty.</li>
<li>A default recognizer cannot be created.</li>
<li>The default recognizer does not support free input.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/496234C1-C20B-46FE-A9BB-4B90C14FEB46">IInkStrokes</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

