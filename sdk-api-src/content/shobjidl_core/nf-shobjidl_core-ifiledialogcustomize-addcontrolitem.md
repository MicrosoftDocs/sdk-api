---
UID: NF:shobjidl_core.IFileDialogCustomize.AddControlItem
title: IFileDialogCustomize::AddControlItem (shobjidl_core.h)
description: Adds an item to a container control in the dialog.
helpviewer_keywords: ["AddControlItem","AddControlItem method [Windows Shell]","AddControlItem method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddControlItem method","IFileDialogCustomize.AddControlItem","IFileDialogCustomize::AddControlItem","shell.IFileDialogCustomize_AddControlItem","shell_IFileDialogCustomize_AddControlItem","shobjidl_core/IFileDialogCustomize::AddControlItem"]
old-location: shell\IFileDialogCustomize_AddControlItem.htm
tech.root: shell
ms.assetid: 56d7d0df-0c3e-4bc3-b91e-3b191f5dad76
ms.date: 12/05/2018
ms.keywords: AddControlItem, AddControlItem method [Windows Shell], AddControlItem method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddControlItem method, IFileDialogCustomize.AddControlItem, IFileDialogCustomize::AddControlItem, shell.IFileDialogCustomize_AddControlItem, shell_IFileDialogCustomize_AddControlItem, shobjidl_core/IFileDialogCustomize::AddControlItem
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
 - IFileDialogCustomize::AddControlItem
 - shobjidl_core/IFileDialogCustomize::AddControlItem
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
 - IFileDialogCustomize.AddControlItem
---

# IFileDialogCustomize::AddControlItem


## -description

Adds an item to a container control in the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

 The ID of the container control to which the item is to be added.

### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the item.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the item's text, which can be either a label or, in the case of a drop-down list, the item itself. This text is a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this item is enabled and visible. Items in control groups cannot be changed after they have been created, with the exception of their enabled and visible states.

Container controls include option button groups, combo boxes, drop-down lists on the <b>Open</b> or <b>Save</b> button, and menus.

