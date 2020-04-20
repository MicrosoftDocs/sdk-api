---
UID: NF:shobjidl_core.IDropTargetHelper.DragLeave
title: IDropTargetHelper::DragLeave (shobjidl_core.h)
description: Notifies the drag-image manager that the drop target's IDropTarget::DragLeave method has been called.helpviewer_keywords: ["DragLeave","DragLeave method [Windows Shell]","DragLeave method [Windows Shell]","IDropTargetHelper interface","IDropTargetHelper interface [Windows Shell]","DragLeave method","IDropTargetHelper.DragLeave","IDropTargetHelper::DragLeave","_win32_IDropTargetHelper_DragLeave","shell.IDropTargetHelper_DragLeave","shobjidl_core/IDropTargetHelper::DragLeave"]
old-location: shell\IDropTargetHelper_DragLeave.htm
tech.root: shell
ms.assetid: a14b56e2-3a90-4802-bb28-869467878c2b
ms.date: 12/05/2018
ms.keywords: DragLeave, DragLeave method [Windows Shell], DragLeave method [Windows Shell],IDropTargetHelper interface, IDropTargetHelper interface [Windows Shell],DragLeave method, IDropTargetHelper.DragLeave, IDropTargetHelper::DragLeave, _win32_IDropTargetHelper_DragLeave, shell.IDropTargetHelper_DragLeave, shobjidl_core/IDropTargetHelper::DragLeave
f1_keywords:
- shobjidl_core/IDropTargetHelper.DragLeave
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IDropTargetHelper.DragLeave
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDropTargetHelper::DragLeave


## -description


Notifies the drag-image manager that the drop target's <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> method has been called.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This method is called by a drop target when its <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave">IDropTarget::DragLeave</a> method is called. It notifies the drag-image manager that the cursor has left the drop target.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper">IDropTargetHelper</a>
 

 

