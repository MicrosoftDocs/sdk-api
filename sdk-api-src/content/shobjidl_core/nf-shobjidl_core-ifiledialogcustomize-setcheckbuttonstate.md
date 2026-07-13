---
UID: NF:shobjidl_core.IFileDialogCustomize.SetCheckButtonState
title: IFileDialogCustomize::SetCheckButtonState (shobjidl_core.h)
description: Sets the state of a check button (check box) in the dialog.
helpviewer_keywords: ["IFileDialogCustomize interface [Windows Shell]","SetCheckButtonState method","IFileDialogCustomize.SetCheckButtonState","IFileDialogCustomize::SetCheckButtonState","SetCheckButtonState","SetCheckButtonState method [Windows Shell]","SetCheckButtonState method [Windows Shell]","IFileDialogCustomize interface","shell.IFileDialogCustomize_SetCheckButtonState","shell_IFileDialogCustomize_SetCheckButtonState","shobjidl_core/IFileDialogCustomize::SetCheckButtonState"]
old-location: shell\IFileDialogCustomize_SetCheckButtonState.htm
tech.root: shell
ms.assetid: b028a811-e559-4152-9081-abaec0cab347
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetCheckButtonState method, IFileDialogCustomize.SetCheckButtonState, IFileDialogCustomize::SetCheckButtonState, SetCheckButtonState, SetCheckButtonState method [Windows Shell], SetCheckButtonState method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetCheckButtonState, shell_IFileDialogCustomize_SetCheckButtonState, shobjidl_core/IFileDialogCustomize::SetCheckButtonState
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
 - IFileDialogCustomize::SetCheckButtonState
 - shobjidl_core/IFileDialogCustomize::SetCheckButtonState
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
 - IFileDialogCustomize.SetCheckButtonState
---

# IFileDialogCustomize::SetCheckButtonState


## -description

Sets the state of a check button (check box) in the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the check box.

### -param bChecked [in]

Type: <b>BOOL</b>

A <b>BOOL</b> value that indicates whether the box is checked. <b>TRUE</b> means checked; <b>FALSE</b>, unchecked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

