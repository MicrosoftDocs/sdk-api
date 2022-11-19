---
UID: NF:oleidl.IDropTarget.DragEnter
title: IDropTarget::DragEnter (oleidl.h)
description: Indicates whether a drop can be accepted, and, if so, the effect of the drop.
helpviewer_keywords: ["DragEnter","DragEnter method [COM]","DragEnter method [COM]","IDropTarget interface","IDropTarget interface [COM]","DragEnter method","IDropTarget.DragEnter","IDropTarget::DragEnter","_ole_idroptarget_dragenter","com.idroptarget_dragenter","oleidl/IDropTarget::DragEnter"]
old-location: com\idroptarget_dragenter.htm
tech.root: com
ms.assetid: 2e4d7013-910c-4a6e-8eee-818e1f2302ac
ms.date: 12/05/2018
ms.keywords: DragEnter, DragEnter method [COM], DragEnter method [COM],IDropTarget interface, IDropTarget interface [COM],DragEnter method, IDropTarget.DragEnter, IDropTarget::DragEnter, _ole_idroptarget_dragenter, com.idroptarget_dragenter, oleidl/IDropTarget::DragEnter
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
 - IDropTarget::DragEnter
 - oleidl/IDropTarget::DragEnter
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
 - IDropTarget.DragEnter
---

# IDropTarget::DragEnter


## -description

Indicates whether a drop can be accepted, and, if so, the effect of the drop.

## -parameters

### -param pDataObj [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object. This data object contains the data being transferred in the drag-and-drop operation. If the drop occurs, this data object will be incorporated into the target.

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
The <i>pdwEffect</i> parameter is <b>NULL</b> on input.

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

You do not call <b>DragEnter</b> directly; instead the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function calls it to determine the effect of a drop the first time the user drags the mouse into the registered window of a drop target.

To implement <b>DragEnter</b>, you must determine whether the target can use the data in the source data object by checking three things:

<ul>
<li>The format and medium specified by the data object</li>
<li>The input value of <i>pdwEffect</i></li>
<li>The state of the modifier keys</li>
</ul>
To check the format and medium, use the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer passed in the <i>pDataObject</i> parameter to call <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumformatetc">IDataObject::EnumFormatEtc</a> so you can enumerate the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures the source data object supports. Then call <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-querygetdata">IDataObject::QueryGetData</a> to determine whether the data object can render the data on the target by examining the formats and medium specified for the data object.

On entry to <b>IDropTarget::DragEnter</b>, the <i>pdwEffect</i> parameter is set to the effects given to the <i>pdwOkEffect</i> parameter of the <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> function. The <b>IDropTarget::DragEnter</b> method must choose one of these effects or disable the drop.

The following modifier keys affect the result of the drop.

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
 

On return, the method must write the effect, one of the DROPEFFECT flags, to the <i>pdwEffect</i> parameter. <a href="/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> then takes this parameter and writes it to its <i>pdwEffect</i> parameter. You communicate the effect of the drop back to the source through <b>DoDragDrop</b> in the <i>pdwEffect</i> parameter. The <b>DoDragDrop</b> function then calls <a href="/windows/desktop/api/oleidl/nf-oleidl-idropsource-givefeedback">IDropSource::GiveFeedback</a> so that the source application can display the appropriate visual feedback to the user through the target window.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">DragEnter</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idropsourcenotify">IDropSourceNotify</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>



<a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a>