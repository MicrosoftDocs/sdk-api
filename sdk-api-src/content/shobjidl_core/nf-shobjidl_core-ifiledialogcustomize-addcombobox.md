---
UID: NF:shobjidl_core.IFileDialogCustomize.AddComboBox
title: IFileDialogCustomize::AddComboBox (shobjidl_core.h)
description: Adds a combo box to the dialog.
helpviewer_keywords: ["AddComboBox","AddComboBox method [Windows Shell]","AddComboBox method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddComboBox method","IFileDialogCustomize.AddComboBox","IFileDialogCustomize::AddComboBox","shell.IFileDialogCustomize_AddComboBox","shell_IFileDialogCustomize_AddComboBox","shobjidl_core/IFileDialogCustomize::AddComboBox"]
old-location: shell\IFileDialogCustomize_AddComboBox.htm
tech.root: shell
ms.assetid: fdb7d682-5182-4bc0-b256-5073bd55c96d
ms.date: 12/05/2018
ms.keywords: AddComboBox, AddComboBox method [Windows Shell], AddComboBox method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddComboBox method, IFileDialogCustomize.AddComboBox, IFileDialogCustomize::AddComboBox, shell.IFileDialogCustomize_AddComboBox, shell_IFileDialogCustomize_AddComboBox, shobjidl_core/IFileDialogCustomize::AddComboBox
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
 - IFileDialogCustomize::AddComboBox
 - shobjidl_core/IFileDialogCustomize::AddComboBox
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
 - IFileDialogCustomize.AddComboBox
---

# IFileDialogCustomize::AddComboBox


## -description

Adds a combo box to the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the combo box to add.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

