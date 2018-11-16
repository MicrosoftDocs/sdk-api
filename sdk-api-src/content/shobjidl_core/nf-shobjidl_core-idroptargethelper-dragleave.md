---
UID: NF:shobjidl_core.IDropTargetHelper.DragLeave
title: IDropTargetHelper::DragLeave
author: windows-sdk-content
description: Notifies the drag-image manager that the drop target's IDropTarget::DragLeave method has been called.
old-location: shell\IDropTargetHelper_DragLeave.htm
tech.root: shell
ms.assetid: a14b56e2-3a90-4802-bb28-869467878c2b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DragLeave, DragLeave method [Windows Shell], DragLeave method [Windows Shell],IDropTargetHelper interface, IDropTargetHelper interface [Windows Shell],DragLeave method, IDropTargetHelper.DragLeave, IDropTargetHelper::DragLeave, _win32_IDropTargetHelper_DragLeave, shell.IDropTargetHelper_DragLeave, shobjidl_core/IDropTargetHelper::DragLeave
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IDropTargetHelper.DragLeave
: 
---

# IDropTargetHelper::DragLeave


## -description


Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> method has been called.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This method is called by a drop target when its <a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">IDropTarget::DragLeave</a> method is called. It notifies the drag-image manager that the cursor has left the drop target.




## -see-also




<a href="https://msdn.microsoft.com/b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0">IDropTargetHelper</a>
 

 

