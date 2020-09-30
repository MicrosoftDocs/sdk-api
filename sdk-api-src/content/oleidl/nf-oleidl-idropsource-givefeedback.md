---
UID: NF:oleidl.IDropSource.GiveFeedback
title: IDropSource::GiveFeedback (oleidl.h)
description: Enables a source application to give visual feedback to the end user during a drag-and-drop operation by providing the DoDragDrop function with an enumeration value specifying the visual effect.
helpviewer_keywords: ["GiveFeedback","GiveFeedback method [COM]","GiveFeedback method [COM]","IDropSource interface","IDropSource interface [COM]","GiveFeedback method","IDropSource.GiveFeedback","IDropSource::GiveFeedback","_ole_idropsource_givefeedback","com.idropsource_givefeedback","oleidl/IDropSource::GiveFeedback"]
old-location: com\idropsource_givefeedback.htm
tech.root: com
ms.assetid: dde37299-ad7c-4f59-af99-e75b72ad9188
ms.date: 12/05/2018
ms.keywords: GiveFeedback, GiveFeedback method [COM], GiveFeedback method [COM],IDropSource interface, IDropSource interface [COM],GiveFeedback method, IDropSource.GiveFeedback, IDropSource::GiveFeedback, _ole_idropsource_givefeedback, com.idropsource_givefeedback, oleidl/IDropSource::GiveFeedback
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
 - IDropSource::GiveFeedback
 - oleidl/IDropSource::GiveFeedback
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
 - IDropSource.GiveFeedback
---

# IDropSource::GiveFeedback


## -description

Enables a source application to give visual feedback to the end user during a drag-and-drop operation by providing the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function with an enumeration value specifying the visual effect.

## -parameters

### -param dwEffect [in]

The <a href="/windows/desktop/com/dropeffect-constants">DROPEFFECT</a> value returned by the most recent call to <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a>, <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a>, or <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a>.

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
<dt><b>DRAGDROP_S_USEDEFAULTCURSORS</b></dt>
</dl>
</td>
<td width="60%">
Indicates successful completion of the method, and requests OLE to update the cursor using the OLE-provided default cursors.

</td>
</tr>
</table>

## -remarks

When your application detects that the user has started a drag-and-drop operation, it should call the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function. <b>DoDragDrop</b> enters a loop, calling <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> when the mouse first enters a drop target window, <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a> when the mouse changes its position within the target window, and <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> when the mouse leaves the target window.

For every call to either <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a>, <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> calls <b>IDropSource::GiveFeedback</b>, passing it the DROPEFFECT value returned from the drop target call.


<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> calls <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> when the mouse has left the target window. Then, <b>DoDragDrop</b> calls <b>IDropSource::GiveFeedback</b> and passes the DROPEFFECT_NONE value in the <i>dwEffect</i> parameter.

The <i>dwEffect</i> parameter can include DROPEFFECT_SCROLL, indicating that the source should put up the drag-scrolling variation of the appropriate pointer.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This function is called frequently during the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> loop, so you can gain performance advantages if you optimize your implementation as much as possible.

<b>IDropSource::GiveFeedback</b> is responsible for changing the cursor shape or for changing the highlighted source based on the value of the <i>dwEffect</i> parameter. If you are using default cursors, you can return DRAGDROP_S_USEDEFAULTCURSORS, which causes OLE to update the cursor for you, using its defaults.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>