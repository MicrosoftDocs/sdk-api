---
UID: NF:oleidl.IDropTarget.DragOver
title: IDropTarget::DragOver (oleidl.h)
description: Provides target feedback to the user and communicates the drop's effect to the DoDragDrop function so it can communicate the effect of the drop back to the source.
helpviewer_keywords: ["DragOver","DragOver method [COM]","DragOver method [COM]","IDropTarget interface","IDropTarget interface [COM]","DragOver method","IDropTarget.DragOver","IDropTarget::DragOver","_ole_idroptarget_dragover","com.idroptarget_dragover","oleidl/IDropTarget::DragOver"]
old-location: com\idroptarget_dragover.htm
tech.root: com
ms.assetid: 31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e
ms.date: 12/05/2018
ms.keywords: DragOver, DragOver method [COM], DragOver method [COM],IDropTarget interface, IDropTarget interface [COM],DragOver method, IDropTarget.DragOver, IDropTarget::DragOver, _ole_idroptarget_dragover, com.idroptarget_dragover, oleidl/IDropTarget::DragOver
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDropTarget::DragOver
 - oleidl/IDropTarget::DragOver
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IDropTarget.DragOver
---

# IDropTarget::DragOver


## -description

Provides target feedback to the user and communicates the drop's effect to the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function so it can communicate the effect of the drop back to the source.

## -parameters

### -param grfKeyState [in]

The current state of the keyboard modifier keys on the keyboard. Valid values can be a combination of any of the flags MK_CONTROL, MK_SHIFT, MK_ALT, MK_BUTTON, MK_LBUTTON, MK_MBUTTON, and MK_RBUTTON.

### -param pt [in]

A <a href="/windows/win32/api/windef/ns-windef-pointl">POINTL</a> structure containing the current cursor coordinates in screen coordinates.

### -param pdwEffect [in, out]

On input, pointer to the value of the <i>pdwEffect</i> parameter of the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function. On return, must contain one of the <a href="/windows/desktop/com/dropeffect-constants">DROPEFFECT</a> flags, which indicates what the result of the drop operation would be.

## -returns

This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwEffect</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

You do not call <b>DragOver</b> directly. The <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls this method each time the user moves the mouse across a given target window. <b>DoDragDrop</b> exits the loop if the drag-and-drop operation is canceled, if the user drags the mouse out of the target window, or if the drop is completed.

In implementing <b>IDropTarget::DragOver</b>, you must provide features similar to those in <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a>. You must determine the effect of dropping the data on the target by examining the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> defining the data object's formats and medium, along with the state of the modifier keys. The mouse position may also play a role in determining the effect of a drop. The following modifier keys affect the result of the drop.

<table>
<tr>
<th>Key Combination</th>
<th>User-Visible Feedback</th>
<th>Drop Effect</th>
</tr>
<tr>
<td>CTRL + SHIFT
</td>
<td>=</td>
<td>DROPEFFECT_LINK
</td>
</tr>
<tr>
<td>CTRL
</td>
<td>+
</td>
<td>DROPEFFECT_COPY
</td>
</tr>
<tr>
<td>No keys or SHIFT
</td>
<td>None
</td>
<td>DROPEFFECT_MOVE
</td>
</tr>
</table>
 

You communicate the effect of the drop back to the source through <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> in <i>pdwEffect</i>. The <b>DoDragDrop</b> function then calls <a href="/windows/desktop/api/oleidl/nf-oleidl-idropsource-givefeedback">IDropSource::GiveFeedback</a> so the source application can display the appropriate visual feedback to the user.

On entry to <b>IDropTarget::DragOver</b>, the <i>pdwEffect</i> parameter must be set to the allowed effects passed to the <i>pdwOkEffect</i> parameter of the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function. The <b>IDropTarget::DragOver</b> method must be able to choose one of these effects or disable the drop.

Upon return, <i>pdwEffect</i> is set to one of the DROPEFFECT flags. This value is then passed to the <i>pdwEffect</i> parameter of <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>. Reasonable values are DROPEFFECT_COPY to copy the dragged data to the target, DROPEFFECT_LINK to create a link to the source data, or DROPEFFECT_MOVE to allow the dragged data to be permanently moved from the source application to the target.

You may also wish to provide appropriate visual feedback in the target window. There may be some target feedback already displayed from a previous call to <b>IDropTarget::DragOver</b> or from the initial <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a>. If this feedback is no longer appropriate, you should remove it.

For efficiency reasons, a data object is not passed in <b>IDropTarget::DragOver</b>. The data object passed in the most recent call to <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> is available and can be used.

When <b>IDropTarget::DragOver</b> has completed its operation, the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls <a href="/windows/desktop/api/oleidl/nf-oleidl-idropsource-givefeedback">IDropSource::GiveFeedback</a> so the source application can display the appropriate visual feedback to the user.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This function is called frequently during the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> loop so it makes sense to optimize your implementation of the <b>DragOver</b> method as much as possible.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>



<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>