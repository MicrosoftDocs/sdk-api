---
UID: NF:ocidl.IOleInPlaceObjectWindowless.GetDropTarget
title: IOleInPlaceObjectWindowless::GetDropTarget (ocidl.h)
description: Retrieves the IDropTarget interface for an in-place active, windowless object that supports drag and drop.
helpviewer_keywords: ["GetDropTarget","GetDropTarget method [COM]","GetDropTarget method [COM]","IOleInPlaceObjectWindowless interface","IOleInPlaceObjectWindowless interface [COM]","GetDropTarget method","IOleInPlaceObjectWindowless.GetDropTarget","IOleInPlaceObjectWindowless::GetDropTarget","_ole_ioleinplaceobjectwindowless_getdroptarget","com.ioleinplaceobjectwindowless_getdroptarget","ocidl/IOleInPlaceObjectWindowless::GetDropTarget"]
old-location: com\ioleinplaceobjectwindowless_getdroptarget.htm
tech.root: com
ms.assetid: 0dfed2c7-d513-4c29-8182-af1bd6f26834
ms.date: 12/05/2018
ms.keywords: GetDropTarget, GetDropTarget method [COM], GetDropTarget method [COM],IOleInPlaceObjectWindowless interface, IOleInPlaceObjectWindowless interface [COM],GetDropTarget method, IOleInPlaceObjectWindowless.GetDropTarget, IOleInPlaceObjectWindowless::GetDropTarget, _ole_ioleinplaceobjectwindowless_getdroptarget, com.ioleinplaceobjectwindowless_getdroptarget, ocidl/IOleInPlaceObjectWindowless::GetDropTarget
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IOleInPlaceObjectWindowless::GetDropTarget
 - ocidl/IOleInPlaceObjectWindowless::GetDropTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceObjectWindowless.GetDropTarget
---

# IOleInPlaceObjectWindowless::GetDropTarget


## -description

Retrieves the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface for an in-place active, windowless object that supports drag and drop.

## -parameters

### -param ppDropTarget [out]

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> pointer variable that receives the interface pointer to the windowless object.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The windowless object does not support drag and drop.

</td>
</tr>
</table>

## -remarks

A windowed object registers its <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface by calling the <a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a> function and supplying its window handle as a parameter. Registering its <b>IDropTarget</b> interface enables the object to participate in drag and drop operations. Because it does not have a window when active, a windowless object cannot register its <b>IDropTarget</b> interface. Therefore, it cannot directly participate in drag and drop operations without support from its container.

The following events occur during a drag and drop operation involving windowless objects:

<ul>
<li>The container registers its own <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface through the <a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a> function.</li>
<li>In the container's implementation of its own <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a> methods, the container detects whether the mouse pointer just entered an embedded object.</li>
<li>If the object is inactive, the container calls the object's <a href="/windows/desktop/api/ocidl/nf-ocidl-ipointerinactive-getactivationpolicy">IPointerInactive::GetActivationPolicy</a> method. The object returns the POINTERINACTIVE_ACTIVATEONDRAG flag. The container then activates the object in place. If the object was already active, the container does not have to do this step.</li>
<li>After the object is active, the container must then obtain the object's <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface.</li>
<li>A windowless object that wishes to be a drop target still implements the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface, but does not register it and does not return it through calls to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>. Instead, the container can obtain this interface by calling the object's <b>IOleInPlaceObjectWindowless::GetDropTarget</b> method. The object returns a pointer to its own <b>IDropTarget</b> interface if it wants to participate in drag and drop operations. The container can cache this interface pointer for later use. For example, on subsequent calls to the container's <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> methods, the container can use the cached pointer instead of calling the object's GetDropTarget method again.</li>
<li>The container then calls the object's <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> and passes the returned value for <i>pdwEffect</i> from its own <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a> or <b>IDropTarget::DragEnter</b> methods. From this point on, the container forwards all subsequent <b>IDropTarget::DragOver</b> calls to the windowless object until the mouse leaves the object or a drop occurs on the object. If the mouse leaves the object, the container calls the object's <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> and then releases the object's <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface. If the drop occurs, the container forwards the <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> call to the object.</li>
<li>Finally, the container in-place deactivates the object.</li>
</ul>
An object can return S_FALSE from its own <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> to indicate that it does not accept any of the data formats in the data object. In that case, the container can decide to accept the data for itself and return an appropriate <i>dwEffect</i> from its own <b>IDropTarget::DragEnter</b> or <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a> methods.

An object that returns S_FALSE from <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> should be prepared to receive subsequent calls to <b>IDropTarget::DragEnter</b> without any <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> in between. Indeed, if the mouse is still over the same object during the next call to the container's <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a>, the container may decide to try and call <b>IDropTarget::DragEnter</b> again on the object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container can cache the pointer to the object's <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface for later use.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless">IOleInPlaceObjectWindowless</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipointerinactive-getactivationpolicy">IPointerInactive::GetActivationPolicy</a>



<a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a>