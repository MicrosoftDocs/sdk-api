---
UID: NF:shobjidl_core.IFileDialogCustomize.AddRadioButtonList
title: IFileDialogCustomize::AddRadioButtonList (shobjidl_core.h)
description: Adds an option button (also known as radio button) group to the dialog.
helpviewer_keywords: ["AddRadioButtonList","AddRadioButtonList method [Windows Shell]","AddRadioButtonList method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddRadioButtonList method","IFileDialogCustomize.AddRadioButtonList","IFileDialogCustomize::AddRadioButtonList","shell.IFileDialogCustomize_AddRadioButtonList","shell_IFileDialogCustomize_AddRadioButtonList","shobjidl_core/IFileDialogCustomize::AddRadioButtonList"]
old-location: shell\IFileDialogCustomize_AddRadioButtonList.htm
tech.root: shell
ms.assetid: 9f60b69d-4625-48b7-b265-ab2e9d842fc2
ms.date: 12/05/2018
ms.keywords: AddRadioButtonList, AddRadioButtonList method [Windows Shell], AddRadioButtonList method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddRadioButtonList method, IFileDialogCustomize.AddRadioButtonList, IFileDialogCustomize::AddRadioButtonList, shell.IFileDialogCustomize_AddRadioButtonList, shell_IFileDialogCustomize_AddRadioButtonList, shobjidl_core/IFileDialogCustomize::AddRadioButtonList
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
 - IFileDialogCustomize::AddRadioButtonList
 - shobjidl_core/IFileDialogCustomize::AddRadioButtonList
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
 - IFileDialogCustomize.AddRadioButtonList
---

# IFileDialogCustomize::AddRadioButtonList


## -description

Adds an option button (also known as radio button) group to the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the option button group to add.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

