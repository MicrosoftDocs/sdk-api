---
UID: NN:shobjidl_core.IDropTargetHelper
title: IDropTargetHelper (shobjidl_core.h)
description: Exposes methods that allow drop targets to display a drag image while the image is over the target window.
helpviewer_keywords: ["IDropTargetHelper","IDropTargetHelper interface [Windows Shell]","IDropTargetHelper interface [Windows Shell]","described","_win32_IDropTargetHelper","shell.IDropTargetHelper","shobjidl_core/IDropTargetHelper"]
old-location: shell\IDropTargetHelper.htm
tech.root: shell
ms.assetid: b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0
ms.date: 12/05/2018
ms.keywords: IDropTargetHelper, IDropTargetHelper interface [Windows Shell], IDropTargetHelper interface [Windows Shell],described, _win32_IDropTargetHelper, shell.IDropTargetHelper, shobjidl_core/IDropTargetHelper
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDropTargetHelper
 - shobjidl_core/IDropTargetHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDropTargetHelper
---

# IDropTargetHelper interface


## -description

Exposes methods that allow drop targets to display a drag image while the image is over the target window.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDropTargetHelper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDropTargetHelper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter">DragEnter</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter">IDropTarget::DragEnter</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave">DragLeave</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover">DragOver</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover">IDropTarget::DragOver</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop">Drop</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager that the drop target's <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> method has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show">Show</a>
</td>
<td align="left" width="63%">
Notifies the drag-image manager to show or hide the drag image.

</td>
</tr>
</table>

## -remarks

This interface is exposed by the Shell's drag-image manager. It is not implemented by applications.

This interface is used by drop targets to enable the drag-image manager to display the drag image while the image is over the target window. The <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a> and <b>IDropTargetHelper</b> interfaces are exposed by the drag-image manager object to allow the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface to use custom drag images. To use either of these interfaces, you must create an in-process server drag-image manager object by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class identifier (CLSID) of CLSID_DragDropHelper. Get interface pointers using standard Component Object Model (COM) procedures.

Four of the <b>IDropTargetHelper</b> methods correspond to the four <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> methods. When you implement <b>IDropTarget</b>, each of its methods should call the corresponding <b>IDropTargetHelper</b> method to pass the information to the drag-image manager. The fifth <b>IDropTargetHelper</b> method notifies the drag-image manager to show or hide the drag image. This method is used when dragging over a target window in a low color-depth video mode. It allows the target to hide the drag image while it is painting the window.

<div class="alert"><b>Note</b>   The drag-and-drop helper object calls <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a> to load private formats—used for cross-process support—into the data object. It later retrieves these formats by calling <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. To support the drag-and-drop helper object, the data object's <b>SetData</b> and <b>GetData</b> implementations must be able to accept and return arbitrary private formats.</div>
<div> </div>
For further discussion of Shell drag-and-drop operations, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776905(v=vs.85)">Transferring Shell Data Using Drag-and-Drop or the Clipboard</a>.

<div class="alert"><b>Note</b>   Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/dataobject">Shell Data Object</a>

