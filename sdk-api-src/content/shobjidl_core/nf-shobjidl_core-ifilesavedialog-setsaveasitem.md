---
UID: NF:shobjidl_core.IFileSaveDialog.SetSaveAsItem
title: IFileSaveDialog::SetSaveAsItem (shobjidl_core.h)
description: Sets an item to be used as the initial entry in a Save As dialog.
helpviewer_keywords: ["IFileSaveDialog interface [Windows Shell]","SetSaveAsItem method","IFileSaveDialog.SetSaveAsItem","IFileSaveDialog::SetSaveAsItem","SetSaveAsItem","SetSaveAsItem method [Windows Shell]","SetSaveAsItem method [Windows Shell]","IFileSaveDialog interface","shell.IFileSaveDialog_SetSaveAsItem","shell_IFileSaveDialog_SetSaveAsItem","shobjidl_core/IFileSaveDialog::SetSaveAsItem"]
old-location: shell\IFileSaveDialog_SetSaveAsItem.htm
tech.root: shell
ms.assetid: aa313685-1334-4899-a55a-6549b48e1464
ms.date: 12/05/2018
ms.keywords: IFileSaveDialog interface [Windows Shell],SetSaveAsItem method, IFileSaveDialog.SetSaveAsItem, IFileSaveDialog::SetSaveAsItem, SetSaveAsItem, SetSaveAsItem method [Windows Shell], SetSaveAsItem method [Windows Shell],IFileSaveDialog interface, shell.IFileSaveDialog_SetSaveAsItem, shell_IFileSaveDialog_SetSaveAsItem, shobjidl_core/IFileSaveDialog::SetSaveAsItem
req.header: shobjidl_core.h
req.include-header: 
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
 - IFileSaveDialog::SetSaveAsItem
 - shobjidl_core/IFileSaveDialog::SetSaveAsItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog.SetSaveAsItem
---

# IFileSaveDialog::SetSaveAsItem


## -description

Sets an item to be used as the initial entry in a <b>Save As</b> dialog.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The name of the item is displayed in the file name edit box, and the containing folder is opened in the view. This would generally be used when the application is saving an item that already exists. For new items, use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfilename">IFileDialog::SetFileName</a>.