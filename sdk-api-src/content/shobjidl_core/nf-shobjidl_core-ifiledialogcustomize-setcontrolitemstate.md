---
UID: NF:shobjidl_core.IFileDialogCustomize.SetControlItemState
title: IFileDialogCustomize::SetControlItemState (shobjidl_core.h)
description: Sets the current state of an item in a container control found in the dialog.
helpviewer_keywords: ["IFileDialogCustomize interface [Windows Shell]","SetControlItemState method","IFileDialogCustomize.SetControlItemState","IFileDialogCustomize::SetControlItemState","SetControlItemState","SetControlItemState method [Windows Shell]","SetControlItemState method [Windows Shell]","IFileDialogCustomize interface","shell.IFileDialogCustomize_SetControlItemState","shell_IFileDialogCustomize_SetControlItemState","shobjidl_core/IFileDialogCustomize::SetControlItemState"]
old-location: shell\IFileDialogCustomize_SetControlItemState.htm
tech.root: shell
ms.assetid: 2570b717-b886-4139-837b-5d71ec16c21e
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetControlItemState method, IFileDialogCustomize.SetControlItemState, IFileDialogCustomize::SetControlItemState, SetControlItemState, SetControlItemState method [Windows Shell], SetControlItemState method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetControlItemState, shell_IFileDialogCustomize_SetControlItemState, shobjidl_core/IFileDialogCustomize::SetControlItemState
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileDialogCustomize::SetControlItemState
 - shobjidl_core/IFileDialogCustomize::SetControlItemState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.SetControlItemState
---

# IFileDialogCustomize::SetControlItemState


## -description

Sets the current state of an item in a container control found in the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the container control.

### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the item.

### -param dwState [in]

Type: <b>CDCONTROLSTATEF</b>

One or more values from the <a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)">CDCONTROLSTATE</a> enumeration that indicate the new state of the control.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state of a control item is enabled and visible. Items in control groups cannot be changed after they have been created, with the exception of their enabled and visible states.

Container controls include option button groups, combo boxes, drop-down lists on the <b>Open</b> or <b>Save</b> button, and menus.