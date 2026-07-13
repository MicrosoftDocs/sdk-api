---
UID: NF:shobjidl_core.IDropTargetHelper.Drop
title: IDropTargetHelper::Drop (shobjidl_core.h)
description: Notifies the drag-image manager that the drop target's IDropTarget::Drop method has been called.
helpviewer_keywords: ["Drop","Drop method [Windows Shell]","Drop method [Windows Shell]","IDropTargetHelper interface","IDropTargetHelper interface [Windows Shell]","Drop method","IDropTargetHelper.Drop","IDropTargetHelper::Drop","_win32_IDropTargetHelper_Drop","shell.IDropTargetHelper_Drop","shobjidl_core/IDropTargetHelper::Drop"]
old-location: shell\IDropTargetHelper_Drop.htm
tech.root: shell
ms.assetid: fe825459-3daa-4e42-b421-302ad6d2a122
ms.date: 12/05/2018
ms.keywords: Drop, Drop method [Windows Shell], Drop method [Windows Shell],IDropTargetHelper interface, IDropTargetHelper interface [Windows Shell],Drop method, IDropTargetHelper.Drop, IDropTargetHelper::Drop, _win32_IDropTargetHelper_Drop, shell.IDropTargetHelper_Drop, shobjidl_core/IDropTargetHelper::Drop
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
 - IDropTargetHelper::Drop
 - shobjidl_core/IDropTargetHelper::Drop
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
 - IDropTargetHelper.Drop
---

# IDropTargetHelper::Drop


## -description

Notifies the drag-image manager that the drop target's <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> method has been called.

## -parameters

### -param pDataObject [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to the data object's <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface.

### -param ppt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure pointer that was received in the <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> method's 
					<i>pt</i> parameter.

### -param dwEffect [in]

Type: <b>DWORD</b>

The value pointed to by the <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> method's 
					<i>pdwEffect</i> parameter.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.

## -remarks

This method is called by a drop target when its <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> method is called. It notifies the drag-image manager that the object has been dropped, and provides it with the information needed to display the drag image.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper">IDropTargetHelper</a>