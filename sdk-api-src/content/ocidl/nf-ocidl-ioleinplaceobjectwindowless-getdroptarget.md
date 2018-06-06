---
UID: NF:ocidl.IOleInPlaceObjectWindowless.GetDropTarget
title: IOleInPlaceObjectWindowless::GetDropTarget
author: windows-sdk-content
description: Retrieves the IDropTarget interface for an in-place active, windowless object that supports drag and drop.
old-location: com\ioleinplaceobjectwindowless_getdroptarget.htm
old-project: com
ms.assetid: 0dfed2c7-d513-4c29-8182-af1bd6f26834
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetDropTarget, GetDropTarget method [COM], GetDropTarget method [COM],IOleInPlaceObjectWindowless interface, IOleInPlaceObjectWindowless interface [COM],GetDropTarget method, IOleInPlaceObjectWindowless.GetDropTarget, IOleInPlaceObjectWindowless::GetDropTarget, _ole_ioleinplaceobjectwindowless_getdroptarget, com.ioleinplaceobjectwindowless_getdroptarget, ocidl/IOleInPlaceObjectWindowless::GetDropTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleInPlaceObjectWindowless.GetDropTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleInPlaceObjectWindowless::GetDropTarget


## -description


Retrieves the <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface for an in-place active, windowless object that supports drag and drop.


## -parameters




### -param ppDropTarget [out]

A pointer to an <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> pointer variable that receives the interface pointer to the windowless object.


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



A windowed object registers its <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface by calling the <a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a> function and supplying its window handle as a parameter. Registering its <b>IDropTarget</b> interface enables the object to participate in drag and drop operations. Because it does not have a window when active, a windowless object cannot register its <b>IDropTarget</b> interface. Therefore, it cannot directly participate in drag and drop operations without support from its container.

The following events occur during a drag and drop operation involving windowless objects:

<ul>
<li>The container registers its own <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface through the <a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a> function.</li>
<li>In the container's implementation of its own <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> or <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> methods, the container detects whether the mouse pointer just entered an embedded object.</li>
<li>
If the object is inactive, the container calls the object's <a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a> method. The object returns the POINTERINACTIVE_ACTIVATEONDRAG flag. The container then activates the object in place. If the object was already active, the container does not have to do this step.</li>
<li>After the object is active, the container must then obtain the object's <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface.</li>
<li>A windowless object that wishes to be a drop target still implements the <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface, but does not register it and does not return it through calls to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>. Instead, the container can obtain this interface by calling the object's <b>IOleInPlaceObjectWindowless::GetDropTarget</b> method. The object returns a pointer to its own <b>IDropTarget</b> interface if it wants to participate in drag and drop operations. The container can cache this interface pointer for later use. For example, on subsequent calls to the container's <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> or <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> methods, the container can use the cached pointer instead of calling the object's GetDropTarget method again.</li>
<li>The container then calls the object's <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> and passes the returned value for <i>pdwEffect</i> from its own <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> or <b>IDropTarget::DragEnter</b> methods. From this point on, the container forwards all subsequent <b>IDropTarget::DragOver</b> calls to the windowless object until the mouse leaves the object or a drop occurs on the object. If the mouse leaves the object, the container calls the object's <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> and then releases the object's <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface. If the drop occurs, the container forwards the <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> call to the object.</li>
<li>Finally, the container in-place deactivates the object.</li>
</ul>
An object can return S_FALSE from its own <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> to indicate that it does not accept any of the data formats in the data object. In that case, the container can decide to accept the data for itself and return an appropriate <i>dwEffect</i> from its own <b>IDropTarget::DragEnter</b> or <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> methods.

An object that returns S_FALSE from <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> should be prepared to receive subsequent calls to <b>IDropTarget::DragEnter</b> without any <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> in between. Indeed, if the mouse is still over the same object during the next call to the container's <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a>, the container may decide to try and call <b>IDropTarget::DragEnter</b> again on the object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container can cache the pointer to the object's <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface for later use.





## -see-also




<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>



<a href="https://msdn.microsoft.com/86aabb46-6bc7-4953-b4eb-8692552ca380">IOleInPlaceObjectWindowless</a>



<a href="https://msdn.microsoft.com/bbdea7e1-620f-4b2b-8ac9-77061b8cfc1a">IPointerInactive::GetActivationPolicy</a>



<a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>
 

 

