---
UID: NF:shobjidl_core.IFileDialogCustomize.AddCheckButton
title: IFileDialogCustomize::AddCheckButton (shobjidl_core.h)
description: Adds a check button (check box) to the dialog.
helpviewer_keywords: ["AddCheckButton","AddCheckButton method [Windows Shell]","AddCheckButton method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddCheckButton method","IFileDialogCustomize.AddCheckButton","IFileDialogCustomize::AddCheckButton","shell.IFileDialogCustomize_AddCheckButton","shell_IFileDialogCustomize_AddCheckButton","shobjidl_core/IFileDialogCustomize::AddCheckButton"]
old-location: shell\IFileDialogCustomize_AddCheckButton.htm
tech.root: shell
ms.assetid: 273ec875-43c1-454f-a4fc-01a513554e68
ms.date: 12/05/2018
ms.keywords: AddCheckButton, AddCheckButton method [Windows Shell], AddCheckButton method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddCheckButton method, IFileDialogCustomize.AddCheckButton, IFileDialogCustomize::AddCheckButton, shell.IFileDialogCustomize_AddCheckButton, shell_IFileDialogCustomize_AddCheckButton, shobjidl_core/IFileDialogCustomize::AddCheckButton
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
 - IFileDialogCustomize::AddCheckButton
 - shobjidl_core/IFileDialogCustomize::AddCheckButton
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
 - IFileDialogCustomize.AddCheckButton
---

# IFileDialogCustomize::AddCheckButton


## -description

Adds a check button (check box) to the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the check button to add.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the button text as a null-terminated Unicode string.

### -param bChecked [in]

Type: <b>BOOL</b>

A <b>BOOL</b> indicating the current state of the check button. <b>TRUE</b> if checked; <b>FALSE</b> otherwise.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

