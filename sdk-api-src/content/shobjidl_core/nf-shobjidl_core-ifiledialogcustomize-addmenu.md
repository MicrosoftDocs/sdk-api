---
UID: NF:shobjidl_core.IFileDialogCustomize.AddMenu
title: IFileDialogCustomize::AddMenu (shobjidl_core.h)
description: Adds a menu to the dialog.
helpviewer_keywords: ["AddMenu","AddMenu method [Windows Shell]","AddMenu method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddMenu method","IFileDialogCustomize.AddMenu","IFileDialogCustomize::AddMenu","shell.IFileDialogCustomize_AddMenu","shell_IFileDialogCustomize_AddMenu","shobjidl_core/IFileDialogCustomize::AddMenu"]
old-location: shell\IFileDialogCustomize_AddMenu.htm
tech.root: shell
ms.assetid: e5e29554-e095-4164-bf67-64f9d6a3e502
ms.date: 12/05/2018
ms.keywords: AddMenu, AddMenu method [Windows Shell], AddMenu method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddMenu method, IFileDialogCustomize.AddMenu, IFileDialogCustomize::AddMenu, shell.IFileDialogCustomize_AddMenu, shell_IFileDialogCustomize_AddMenu, shobjidl_core/IFileDialogCustomize::AddMenu
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
 - IFileDialogCustomize::AddMenu
 - shobjidl_core/IFileDialogCustomize::AddMenu
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
 - IFileDialogCustomize.AddMenu
---

# IFileDialogCustomize::AddMenu


## -description

Adds a menu to the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the menu to add.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the menu name as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

To add items to this control, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addcontrolitem">IFileDialogCustomize::AddControlItem</a>.