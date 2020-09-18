---
UID: NF:oleidl.IDropSource.QueryContinueDrag
title: IDropSource::QueryContinueDrag (oleidl.h)
description: Determines whether a drag-and-drop operation should be continued, canceled, or completed. You do not call this method directly. The OLE DoDragDrop function calls this method during a drag-and-drop operation.
helpviewer_keywords: ["IDropSource interface [COM]","QueryContinueDrag method","IDropSource.QueryContinueDrag","IDropSource::QueryContinueDrag","QueryContinueDrag","QueryContinueDrag method [COM]","QueryContinueDrag method [COM]","IDropSource interface","_ole_idropsource_querycontinuedrag","com.idropsource_querycontinuedrag","oleidl/IDropSource::QueryContinueDrag"]
old-location: com\idropsource_querycontinuedrag.htm
tech.root: com
ms.assetid: 96ea44fc-5046-4e31-abfc-659d8ef3ca8f
ms.date: 12/05/2018
ms.keywords: IDropSource interface [COM],QueryContinueDrag method, IDropSource.QueryContinueDrag, IDropSource::QueryContinueDrag, QueryContinueDrag, QueryContinueDrag method [COM], QueryContinueDrag method [COM],IDropSource interface, _ole_idropsource_querycontinuedrag, com.idropsource_querycontinuedrag, oleidl/IDropSource::QueryContinueDrag
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
 - IDropSource::QueryContinueDrag
 - oleidl/IDropSource::QueryContinueDrag
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
 - IDropSource.QueryContinueDrag
---

# IDropSource::QueryContinueDrag


## -description

Determines whether a drag-and-drop operation should be continued, canceled, or completed. You do not call this method directly. The OLE <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls this method during a drag-and-drop operation.

## -parameters

### -param fEscapePressed [in]

Indicates whether the Esc key has been pressed since the previous call to <b>QueryContinueDrag</b> or to <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> if this is the first call to <b>QueryContinueDrag</b>. A <b>TRUE</b> value indicates the end user has pressed the escape key; a <b>FALSE</b> value indicates it has not been pressed.

### -param grfKeyState [in]

The current state of the keyboard modifier keys on the keyboard. Possible values can be a combination of any of the flags MK_CONTROL, MK_SHIFT, MK_ALT, MK_BUTTON, MK_LBUTTON, MK_MBUTTON, and MK_RBUTTON.

## -returns

This method can return the following values.

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
The drag operation should continue. This result occurs if no errors are detected, the mouse button starting the drag-and-drop operation has not been released, and the Esc key has not been detected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_DROP</b></dt>
</dl>
</td>
<td width="60%">
The drop operation should occur completing the drag operation. This result occurs if <i>grfKeyState</i> indicates that the key that started the drag-and-drop operation has been released.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The drag operation should be canceled with no drop operation occurring. This result occurs if <i>fEscapePressed</i> is <b>TRUE</b>, indicating the Esc key has been pressed.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls <b>QueryContinueDrag</b> whenever it detects a change in the keyboard or mouse button state during a drag-and-drop operation. <b>QueryContinueDrag</b> must determine whether the drag-and-drop operation should be continued, canceled, or completed based on the contents of the parameters <i>grfKeyState</i> and <i>fEscapePressed</i>.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>