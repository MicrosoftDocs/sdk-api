---
UID: NF:msinkaut.IInkDisp.ClipboardCopy
title: IInkDisp::ClipboardCopy
author: windows-sdk-content
description: Copies the InkStrokes collection to the Clipboard.
old-location: tablet\inkdisp_clipboardcopy.htm
tech.root: tablet
ms.assetid: ad62c9b3-6df6-445b-9085-7cd5c4b6b31f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ClipboardCopy, ClipboardCopy method [Tablet PC], ClipboardCopy method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ClipboardCopy method, IInkDisp.ClipboardCopy, IInkDisp::ClipboardCopy, ad62c9b3-6df6-445b-9085-7cd5c4b6b31f, msinkaut/IInkDisp::ClipboardCopy, tablet.inkdisp_clipboardcopy
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
 - IInkDisp.ClipboardCopy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDisp::ClipboardCopy


## -description



Copies the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to the Clipboard.




## -parameters




### -param strokes [in, optional]

Optional. Specifies the strokes to copy. If the strokes parameter is <b>NULL</b>, the <b>ClipboardCopy</b> method copies the entire <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. The default value is <b>NULL</b>.


### -param ClipboardFormats [in, optional]

Optional. Specifies the <a href="https://msdn.microsoft.com/bedee31c-d957-4162-83d9-f1c8df9428cd">InkClipboardFormats</a> enumeration value of the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. The default value is <b>ICF_Default</b>.


### -param ClipboardModes [in, optional]

Optional. Specifies the <a href="https://msdn.microsoft.com/a9718b79-8f98-4bfc-a5db-208899d1f59e">InkClipboardModes</a> enumeration value of the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. The default value is <b>ICB_Default</b>.


### -param DataObject [out, retval]

When this method returns, contains a pointer to the newly create data object.


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
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The strokes parameter is associated with a different Ink object.

</td>
</tr>
</table>
 




## -remarks



This method copies all properties of the stroke, including recognition results. Setting the <i>strokes</i> parameter to <b>NULL</b> copies the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object to the Clipboard, including the <a href="https://msdn.microsoft.com/33425e5b-2ba0-4026-ab19-33579e7bb9f5">CustomStrokes</a> property, and recognition results for strokes in the <b>InkDisp</b> object's <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes</a> collection are maintained.

If an empty <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection is passed, the method returns <b>NULL</b> and the contents of the Clipboard are not modified.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize(NULL)</a> must be called before the clipboard APIs can work.</div>
<div> </div>
<div class="alert"><b>Caution</b>  To avoid potential memory leaks as a result of using the <a href="https://msdn.microsoft.com/a9718b79-8f98-4bfc-a5db-208899d1f59e">ICB_DelayedCopy</a> flag, you must call the <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a> or <a href="https://msdn.microsoft.com/741def10-d2b5-4395-8049-1eba2e29b0e8">OleSetClipboard</a> method. This must be done before the application exits if the last call to the <b>ClipboardCopy</b> method used the <b>ICB_DelayedCopy</b> flag.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a4e6a183-242a-40af-871b-43a0b177a27a">ClipboardCopyWithRectangle Method</a>



<a href="https://msdn.microsoft.com/85B683AA-D859-4717-8C61-C0EB4BBA5F61">IInkDisp</a>



<a href="https://msdn.microsoft.com/bedee31c-d957-4162-83d9-f1c8df9428cd">InkClipboardFormats Enumeration</a>



<a href="https://msdn.microsoft.com/a9718b79-8f98-4bfc-a5db-208899d1f59e">InkClipboardModes Enumeration</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

