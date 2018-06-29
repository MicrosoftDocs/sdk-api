---
UID: NF:shobjidl_core.IDropTargetHelper.Drop
title: IDropTargetHelper::Drop
author: windows-sdk-content
description: Notifies the drag-image manager that the drop target's IDropTarget::Drop method has been called.
old-location: shell\IDropTargetHelper_Drop.htm
old-project: shell
ms.assetid: fe825459-3daa-4e42-b421-302ad6d2a122
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: Drop, Drop method [Windows Shell], Drop method [Windows Shell],IDropTargetHelper interface, IDropTargetHelper interface [Windows Shell],Drop method, IDropTargetHelper.Drop, IDropTargetHelper::Drop, _win32_IDropTargetHelper_Drop, shell.IDropTargetHelper_Drop, shobjidl_core/IDropTargetHelper::Drop
ms.prod: windows
ms.technology: windows-sdk
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
 - IDropTargetHelper.Drop
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDropTargetHelper::Drop


## -description


Notifies the drag-image manager that the drop target's <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> method has been called.


## -parameters




### -param pDataObject [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the data object's <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface.


### -param ppt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure pointer that was received in the <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> method's 
					<i>pt</i> parameter.


### -param dwEffect [in]

Type: <b>DWORD</b>

The value pointed to by the <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> method's 
					<i>pdwEffect</i> parameter.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This method is called by a drop target when its <a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">IDropTarget::Drop</a> method is called. It notifies the drag-image manager that the object has been dropped, and provides it with the information needed to display the drag image.




## -see-also




<a href="https://msdn.microsoft.com/b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0">IDropTargetHelper</a>
 

 

