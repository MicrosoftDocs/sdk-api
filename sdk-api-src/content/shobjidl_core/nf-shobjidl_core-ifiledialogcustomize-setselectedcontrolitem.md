---
UID: NF:shobjidl_core.IFileDialogCustomize.SetSelectedControlItem
title: IFileDialogCustomize::SetSelectedControlItem (shobjidl_core.h)
description: Sets the selected state of a particular item in an option button group or a combo box found in the dialog.
helpviewer_keywords: ["IFileDialogCustomize interface [Windows Shell]","SetSelectedControlItem method","IFileDialogCustomize.SetSelectedControlItem","IFileDialogCustomize::SetSelectedControlItem","SetSelectedControlItem","SetSelectedControlItem method [Windows Shell]","SetSelectedControlItem method [Windows Shell]","IFileDialogCustomize interface","shell.IFileDialogCustomize_SetSelectedControlItem","shell_IFileDialogCustomize_SetSelectedControlItem","shobjidl_core/IFileDialogCustomize::SetSelectedControlItem"]
old-location: shell\IFileDialogCustomize_SetSelectedControlItem.htm
tech.root: shell
ms.assetid: ff0287db-fdd8-415c-9c78-607ec79b5e2d
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetSelectedControlItem method, IFileDialogCustomize.SetSelectedControlItem, IFileDialogCustomize::SetSelectedControlItem, SetSelectedControlItem, SetSelectedControlItem method [Windows Shell], SetSelectedControlItem method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetSelectedControlItem, shell_IFileDialogCustomize_SetSelectedControlItem, shobjidl_core/IFileDialogCustomize::SetSelectedControlItem
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
 - IFileDialogCustomize::SetSelectedControlItem
 - shobjidl_core/IFileDialogCustomize::SetSelectedControlItem
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
 - IFileDialogCustomize.SetSelectedControlItem
---

# IFileDialogCustomize::SetSelectedControlItem


## -description

Sets the selected state of a particular item in an option button group or a combo box found in the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the container control.

### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the item to display as selected in the control.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

