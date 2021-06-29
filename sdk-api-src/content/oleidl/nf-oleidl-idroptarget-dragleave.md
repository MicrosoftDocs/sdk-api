---
UID: NF:oleidl.IDropTarget.DragLeave
title: IDropTarget::DragLeave (oleidl.h)
description: Removes target feedback and releases the data object.
helpviewer_keywords: ["DragLeave","DragLeave method [COM]","DragLeave method [COM]","IDropTarget interface","IDropTarget interface [COM]","DragLeave method","IDropTarget.DragLeave","IDropTarget::DragLeave","_ole_idroptarget_dragleave","com.idroptarget_dragleave","oleidl/IDropTarget::DragLeave"]
old-location: com\idroptarget_dragleave.htm
tech.root: com
ms.assetid: 2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8
ms.date: 12/05/2018
ms.keywords: DragLeave, DragLeave method [COM], DragLeave method [COM],IDropTarget interface, IDropTarget interface [COM],DragLeave method, IDropTarget.DragLeave, IDropTarget::DragLeave, _ole_idroptarget_dragleave, com.idroptarget_dragleave, oleidl/IDropTarget::DragLeave
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
 - IDropTarget::DragLeave
 - oleidl/IDropTarget::DragLeave
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
 - IDropTarget.DragLeave
---

# IDropTarget::DragLeave


## -description

Removes target feedback and releases the data object.



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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

You do not call this method directly. The <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls this method in either of the following cases:

<ul>
<li>When the user drags the cursor out of a given target window.</li>
<li>When the user cancels the current drag-and-drop operation.</li>
</ul>
To implement <b>IDropTarget::DragLeave</b>, you must remove any target feedback that is currently displayed. You must also release any references you hold to the data transfer object.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>



<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>
