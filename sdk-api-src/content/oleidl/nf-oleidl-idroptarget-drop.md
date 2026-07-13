---
UID: NF:oleidl.IDropTarget.Drop
title: IDropTarget::Drop (oleidl.h)
description: Incorporates the source data into the target window, removes target feedback, and releases the data object.
helpviewer_keywords: ["Drop","Drop method [COM]","Drop method [COM]","IDropTarget interface","IDropTarget interface [COM]","Drop method","IDropTarget.Drop","IDropTarget::Drop","_ole_idroptarget_drop","com.idroptarget_drop","oleidl/IDropTarget::Drop"]
old-location: com\idroptarget_drop.htm
tech.root: com
ms.assetid: 7ea6d815-bf8f-47d5-99d3-f9a55bafee2e
ms.date: 12/05/2018
ms.keywords: Drop, Drop method [COM], Drop method [COM],IDropTarget interface, IDropTarget interface [COM],Drop method, IDropTarget.Drop, IDropTarget::Drop, _ole_idroptarget_drop, com.idroptarget_drop, oleidl/IDropTarget::Drop
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
 - IDropTarget::Drop
 - oleidl/IDropTarget::Drop
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
 - IDropTarget.Drop
---

# IDropTarget::Drop


## -description

Incorporates the source data into the target window, removes target feedback, and releases the data object.

## -parameters

### -param pDataObj [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object being transferred in the drag-and-drop operation.

### -param grfKeyState [in]

The current state of the keyboard modifier keys on the keyboard. Possible values can be a combination of any of the flags MK_CONTROL, MK_SHIFT, MK_ALT, MK_BUTTON, MK_LBUTTON, MK_MBUTTON, and MK_RBUTTON.

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
<dt><b>DRAGDROP_S_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The OLE drag-and-drop operation was canceled.

</td>
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
The <i>pdwEffect</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

You do not call this method directly. The <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls this method when the user completes the drag-and-drop operation.

In implementing <b>Drop</b>, you must incorporate the data object into the target. Use the formats available in <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, available through <i>pDataObj</i>, along with the current state of the modifier keys to determine how the data is to be incorporated, such as linking or embedding.

In addition to incorporating the data, you must also clean up as you do in the <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> method:

<ul>
<li>Remove any target feedback that is currently displayed.</li>
<li>Release any references to the data object.</li>
</ul>
You also pass the effect of this operation back to the source application through <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>, so the source application can clean up after the drag-and-drop operation is complete:

<ul>
<li>Remove any source feedback that is being displayed.</li>
<li>Make any necessary changes to the data, such as removing the data if the operation was a move.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>



<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>