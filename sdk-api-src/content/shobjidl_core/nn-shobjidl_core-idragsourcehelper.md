---
UID: NN:shobjidl_core.IDragSourceHelper
title: IDragSourceHelper (shobjidl_core.h)
description: Exposed by the Shell to allow an application to specify the image that will be displayed during a Shell drag-and-drop operation.
helpviewer_keywords: ["IDragSourceHelper","IDragSourceHelper interface [Windows Shell]","IDragSourceHelper interface [Windows Shell]","described","_win32_IDragSourceHelper","shell.IDragSourceHelper","shobjidl_core/IDragSourceHelper"]
old-location: shell\IDragSourceHelper.htm
tech.root: shell
ms.assetid: d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28
ms.date: 12/05/2018
ms.keywords: IDragSourceHelper, IDragSourceHelper interface [Windows Shell], IDragSourceHelper interface [Windows Shell],described, _win32_IDragSourceHelper, shell.IDragSourceHelper, shobjidl_core/IDragSourceHelper
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
 - IDragSourceHelper
 - shobjidl_core/IDragSourceHelper
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
 - IDragSourceHelper
---

# IDragSourceHelper interface


## -description

Exposed by the Shell to allow an application to specify the image that will be displayed during a Shell drag-and-drop operation.

## -inheritance

The <b>IDragSourceHelper</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDragSourceHelper</b> also has these types of members:

## -remarks

This interface is exposed by the Shell's drag-image manager. It is not implemented by applications.

Use this interface to specify the image displayed during a Shell drag-and-drop operation. The <b>IDragSourceHelper</b>,  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper">IDropTargetHelper</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow">IInitializeWithWindow</a> interfaces are exposed by the drag-image manager object to allow the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface to use custom drag images. To use either of these interfaces, you must create an in-process server drag-image manager object by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with a class identifier (CLSID) of CLSID_DragDropHelper. Get interface pointers using standard Component Object Model (COM) procedures.

The <b>IDragSourceHelper</b> interface provides the following two ways to specify the bitmap to be used as a drag image.

				

<ul>
<li>Controls that have a window can register a DI_GETDRAGIMAGE window message for it and initialize the drag-image manager with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow">IDragSourceHelper::InitializeFromWindow</a>. When the DI_GETDRAGIMAGE message is received, the handler puts the drag image bitmap information in the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shdragimage">SHDRAGIMAGE</a> structure that is passed as the message's <i>lParam</i> value.</li>
<li>Windowless controls can initialize the drag-image manager with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap">IDragSourceHelper::InitializeFromBitmap</a>. This method allows an application to simply specify the bitmap.</li>
</ul>
<div class="alert"><b>Note</b>   The drag-and-drop helper object calls <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a> to load private formats—used for cross-process support—into the data object. It later retrieves these formats by calling <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. To support the drag-and-drop helper object, the data object's <b>SetData</b> and <b>GetData</b> implementations must be able to accept and return arbitrary private formats.</div>
<div> </div>
For further discussion of Shell drag-and-drop operations, see <a href="/previous-versions/windows/desktop/legacy/bb776905(v=vs.85)">Transferring Shell Data Using Drag-and-Drop or the Clipboard</a>.

<div class="alert"><b>Note</b>   Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
