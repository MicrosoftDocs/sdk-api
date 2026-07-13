---
UID: NF:shobjidl_core.IFileDialogCustomize.AddSeparator
title: IFileDialogCustomize::AddSeparator (shobjidl_core.h)
description: Adds a separator to the dialog, allowing a visual separation of controls.
helpviewer_keywords: ["AddSeparator","AddSeparator method [Windows Shell]","AddSeparator method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddSeparator method","IFileDialogCustomize.AddSeparator","IFileDialogCustomize::AddSeparator","shell.IFileDialogCustomize_AddSeparator","shell_IFileDialogCustomize_AddSeparator","shobjidl_core/IFileDialogCustomize::AddSeparator"]
old-location: shell\IFileDialogCustomize_AddSeparator.htm
tech.root: shell
ms.assetid: e2d0f1c7-9296-4651-8910-89dcfe5a6a68
ms.date: 12/05/2018
ms.keywords: AddSeparator, AddSeparator method [Windows Shell], AddSeparator method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddSeparator method, IFileDialogCustomize.AddSeparator, IFileDialogCustomize::AddSeparator, shell.IFileDialogCustomize_AddSeparator, shell_IFileDialogCustomize_AddSeparator, shobjidl_core/IFileDialogCustomize::AddSeparator
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
 - IFileDialogCustomize::AddSeparator
 - shobjidl_core/IFileDialogCustomize::AddSeparator
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
 - IFileDialogCustomize.AddSeparator
---

# IFileDialogCustomize::AddSeparator


## -description

Adds a separator to the dialog, allowing a visual separation of controls.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The control ID of the separator.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

