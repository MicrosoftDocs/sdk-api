---
UID: NF:shobjidl_core.IDropTargetHelper.DragOver
title: IDropTargetHelper::DragOver
author: windows-sdk-content
description: Notifies the drag-image manager that the drop target's IDropTarget::DragOver method has been called.
old-location: shell\IDropTargetHelper_DragOver.htm
tech.root: shell
ms.assetid: 92550642-ca77-4a32-ba97-93419b4e5ac7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DragOver, DragOver method [Windows Shell], DragOver method [Windows Shell],IDropTargetHelper interface, IDropTargetHelper interface [Windows Shell],DragOver method, IDropTargetHelper.DragOver, IDropTargetHelper::DragOver, _win32_IDropTargetHelper_DragOver, shell.IDropTargetHelper_DragOver, shobjidl_core/IDropTargetHelper::DragOver
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
 - IDropTargetHelper.DragOver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDropTargetHelper::DragOver


## -description


Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> method has been called.


## -parameters




### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>*</b>

The <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure pointer that was received in the <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> method's 
					<i>pt</i> parameter.


### -param dwEffect [in]

Type: <b>DWORD</b>

The value pointed to by the <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> method's 
					<i>pdwEffect</i> parameter.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This method is called by a drop target when its <a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">IDropTarget::DragOver</a> method is called. It notifies the drag-image manager that the cursor position has changed and provides it with the information needed to display the drag image.
      




## -see-also




<a href="https://msdn.microsoft.com/b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0">IDropTargetHelper</a>
 

 

