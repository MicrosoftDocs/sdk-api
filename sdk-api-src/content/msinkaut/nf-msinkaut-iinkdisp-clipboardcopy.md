---
UID: NF:msinkaut.IInkDisp.ClipboardCopy
title: IInkDisp::ClipboardCopy (msinkaut.h)
description: Copies the InkStrokes collection to the Clipboard.
helpviewer_keywords: ["ClipboardCopy","ClipboardCopy method [Tablet PC]","ClipboardCopy method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","ClipboardCopy method","IInkDisp.ClipboardCopy","IInkDisp::ClipboardCopy","ad62c9b3-6df6-445b-9085-7cd5c4b6b31f","msinkaut/IInkDisp::ClipboardCopy","tablet.inkdisp_clipboardcopy"]
old-location: tablet\inkdisp_clipboardcopy.htm
tech.root: tablet
ms.assetid: ad62c9b3-6df6-445b-9085-7cd5c4b6b31f
ms.date: 12/05/2018
ms.keywords: ClipboardCopy, ClipboardCopy method [Tablet PC], ClipboardCopy method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ClipboardCopy method, IInkDisp.ClipboardCopy, IInkDisp::ClipboardCopy, ad62c9b3-6df6-445b-9085-7cd5c4b6b31f, msinkaut/IInkDisp::ClipboardCopy, tablet.inkdisp_clipboardcopy
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
 - IInkDisp::ClipboardCopy
 - msinkaut/IInkDisp::ClipboardCopy
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
 - IInkDisp.ClipboardCopy
---

# IInkDisp::ClipboardCopy


## -description

Copies the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to the Clipboard.

## -parameters

### -param strokes [in, optional]

Optional. Specifies the strokes to copy. If the strokes parameter is <b>NULL</b>, the <b>ClipboardCopy</b> method copies the entire <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The default value is <b>NULL</b>.

### -param ClipboardFormats [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats">InkClipboardFormats</a> enumeration value of the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The default value is <b>ICF_Default</b>.

### -param ClipboardModes [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">InkClipboardModes</a> enumeration value of the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The default value is <b>ICB_Default</b>.

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

This method copies all properties of the stroke, including recognition results. Setting the <i>strokes</i> parameter to <b>NULL</b> copies the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object to the Clipboard, including the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes">CustomStrokes</a> property, and recognition results for strokes in the <b>InkDisp</b> object's <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection are maintained.

If an empty <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection is passed, the method returns <b>NULL</b> and the contents of the Clipboard are not modified.

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize(NULL)</a> must be called before the clipboard APIs can work.</div>
<div> </div>
<div class="alert"><b>Caution</b>  To avoid potential memory leaks as a result of using the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">ICB_DelayedCopy</a> flag, you must call the <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> or <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> method. This must be done before the application exits if the last call to the <b>ClipboardCopy</b> method used the <b>ICB_DelayedCopy</b> flag.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle">ClipboardCopyWithRectangle Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats">InkClipboardFormats Enumeration</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">InkClipboardModes Enumeration</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
