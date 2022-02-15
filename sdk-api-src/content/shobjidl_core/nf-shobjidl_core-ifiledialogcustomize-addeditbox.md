---
UID: NF:shobjidl_core.IFileDialogCustomize.AddEditBox
title: IFileDialogCustomize::AddEditBox (shobjidl_core.h)
description: Adds an edit box control to the dialog.
helpviewer_keywords: ["AddEditBox","AddEditBox method [Windows Shell]","AddEditBox method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddEditBox method","IFileDialogCustomize.AddEditBox","IFileDialogCustomize::AddEditBox","shell.IFileDialogCustomize_AddEditBox","shell_IFileDialogCustomize_AddEditBox","shobjidl_core/IFileDialogCustomize::AddEditBox"]
old-location: shell\IFileDialogCustomize_AddEditBox.htm
tech.root: shell
ms.assetid: 7648eb7a-d7c4-4d4f-a347-52eb81135270
ms.date: 12/05/2018
ms.keywords: AddEditBox, AddEditBox method [Windows Shell], AddEditBox method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddEditBox method, IFileDialogCustomize.AddEditBox, IFileDialogCustomize::AddEditBox, shell.IFileDialogCustomize_AddEditBox, shell_IFileDialogCustomize_AddEditBox, shobjidl_core/IFileDialogCustomize::AddEditBox
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
 - IFileDialogCustomize::AddEditBox
 - shobjidl_core/IFileDialogCustomize::AddEditBox
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
 - IFileDialogCustomize.AddEditBox
---

# IFileDialogCustomize::AddEditBox


## -description

Adds an edit box control to the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the edit box to add.

### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that provides the default text displayed in the edit box.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

To add a label next to the edit box, place it in a visual group with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-startvisualgroup">IFileDialogCustomize::StartVisualGroup</a>.