---
UID: NN:shobjidl_core.IDropTargetHelper
title: IDropTargetHelper
author: windows-sdk-content
description: Exposes methods that allow drop targets to display a drag image while the image is over the target window.
old-location: shell\IDropTargetHelper.htm
old-project: shell
ms.assetid: b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDropTargetHelper, IDropTargetHelper interface [Windows Shell], IDropTargetHelper interface [Windows Shell],described, _win32_IDropTargetHelper, shell.IDropTargetHelper, shobjidl_core/IDropTargetHelper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDropTargetHelper
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDropTargetHelper interface


## -description


Exposes methods that allow drop targets to display a drag image while the image is over the target window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDropTargetHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDropTargetHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDropTargetHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc0fd3f2-424e-4448-b589-fc4b8dc75506">DragEnter</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">IDropTarget::DragEnter</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a14b56e2-3a90-4802-bb28-869467878c2b">DragLeave</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92550642-ca77-4a32-ba97-93419b4e5ac7">DragOver</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe825459-3daa-4e42-b421-302ad6d2a122">Drop</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/412a87d6-4915-4791-b109-060cc967dbc9">Show</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager to show or hide the drag image.

</td>
</tr>
</table> 


## -remarks



This interface is exposed by the Shell's drag-image manager. It is not implemented by applications.

This interface is used by drop targets to enable the drag-image manager to display the drag image while the image is over the target window. The <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> and <b>IDropTargetHelper</b> interfaces are exposed by the drag-image manager object to allow the <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface to use custom drag images. To use either of these interfaces, you must create an in-process server drag-image manager object by calling <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with a class identifier (CLSID) of CLSID_DragDropHelper. Get interface pointers using standard Component Object Model (COM) procedures.

Four of the <b>IDropTargetHelper</b> methods correspond to the four <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> methods. When you implement <b>IDropTarget</b>, each of its methods should call the corresponding <b>IDropTargetHelper</b> method to pass the information to the drag-image manager. The fifth <b>IDropTargetHelper</b> method notifies the drag-image manager to show or hide the drag image. This method is used when dragging over a target window in a low color-depth video mode. It allows the target to hide the drag image while it is painting the window.

<div class="alert"><b>Note</b>   The drag-and-drop helper object calls <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a> to load private formats—used for cross-process support—into the data object. It later retrieves these formats by calling <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. To support the drag-and-drop helper object, the data object's <b>SetData</b> and <b>GetData</b> implementations must be able to accept and return arbitrary private formats.</div>
<div> </div>
For further discussion of Shell drag-and-drop operations, see <a href="https://msdn.microsoft.com/bd73098b-2f69-48a4-bb06-e1e0a452e69d">Transferring Shell Data Using Drag-and-Drop or the Clipboard</a>.

<div class="alert"><b>Note</b>   Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a>



<a href="https://msdn.microsoft.com/c63d339e-ac62-4da1-b5ce-22d45a6a3413">Shell Data Object</a>
 

 

