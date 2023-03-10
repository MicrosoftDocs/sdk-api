---
UID: NF:msinkaut.IInkDisp.ClipboardCopyWithRectangle
title: IInkDisp::ClipboardCopyWithRectangle (msinkaut.h)
description: Copies the IInkStrokeDisp objects that are contained within the known rectangle to the Clipboard.
helpviewer_keywords: ["ClipboardCopyWithRectangle","ClipboardCopyWithRectangle method [Tablet PC]","ClipboardCopyWithRectangle method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","ClipboardCopyWithRectangle method","IInkDisp.ClipboardCopyWithRectangle","IInkDisp::ClipboardCopyWithRectangle","a4e6a183-242a-40af-871b-43a0b177a27a","msinkaut/IInkDisp::ClipboardCopyWithRectangle","tablet.inkdisp_clipboardcopywithrectangle"]
old-location: tablet\inkdisp_clipboardcopywithrectangle.htm
tech.root: tablet
ms.assetid: a4e6a183-242a-40af-871b-43a0b177a27a
ms.date: 12/05/2018
ms.keywords: ClipboardCopyWithRectangle, ClipboardCopyWithRectangle method [Tablet PC], ClipboardCopyWithRectangle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ClipboardCopyWithRectangle method, IInkDisp.ClipboardCopyWithRectangle, IInkDisp::ClipboardCopyWithRectangle, a4e6a183-242a-40af-871b-43a0b177a27a, msinkaut/IInkDisp::ClipboardCopyWithRectangle, tablet.inkdisp_clipboardcopywithrectangle
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
 - IInkDisp::ClipboardCopyWithRectangle
 - msinkaut/IInkDisp::ClipboardCopyWithRectangle
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
 - IInkDisp.ClipboardCopyWithRectangle
---

# IInkDisp::ClipboardCopyWithRectangle


## -description

Copies the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects that are contained within the known rectangle to the Clipboard.

## -parameters

### -param Rectangle [in]

Specifies the rectangle that contains the strokes to copy to the Clipboard.

### -param ClipboardFormats [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats">InkClipboardFormats</a> enumeration value of the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The default value is <b>ICF_Default</b>.

### -param ClipboardModes [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">InkClipboardModes Enumeration</a> value of the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> object. The default value is <b>ICB_Default</b>.

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
</table>

## -remarks

If the rectangle clips strokes, those strokes are clipped in the copied data.

It may be useful to copy an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object to the Clipboard when you only want to copy the properties of the <b>InkDisp</b> object. To copy an <b>InkDisp</b> object to the Clipboard, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy">ClipboardCopy</a> method with the <i>strokes</i> parameter set to <b>NULL</b>.

<div class="alert"><b>Caution</b>  To avoid potential memory leaks as a result of using the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">ICB_DelayedCopy</a> flag, you must call the <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> or <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> method. This must be done before the application exits if the last call to the <b>ClipboardCopyWithRectangle</b> method used the <b>ICB_DelayedCopy</b> flag.</div>
<div> </div>
When <b>ClipboardCopyWithRectangle</b> is used in <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">ICB_Cut</a> mode, a stroke that gets split into two or more strokes is deleted and new strokes are added in its place.

In addition, the <a href="/windows/desktop/tablet/inkdisp-inkadded">InkAdded</a> and <a href="/windows/desktop/tablet/inkdisp-inkdeleted">InkDeleted</a> events are generated based on the indices of the strokes. For example, if the strokes at indices 0,1,3,5, and 6 are to be deleted, two events will be generated; one for strokes with indices 0123 and one for strokes with indices 5 and 6. That is, one event for each contiguous set.

This also applies to <a href="/windows/desktop/tablet/inkdisp-inkadded">InkAdded</a> events. An internal algorithm determines the indices of the newly added strokes in the stroke collection and this has an impact on how the <b>InkAdded</b> events are fired as described above.

If the strokes count is queried within the event handler, the result is the total number of strokes added by the whole operation including the strokes that have not yet generated events.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy">ClipboardCopy Method</a>



<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats">InkClipboardFormats Enumeration</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardmodes">InkClipboardModes Enumeration</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
