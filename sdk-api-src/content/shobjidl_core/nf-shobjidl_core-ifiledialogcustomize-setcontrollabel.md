---
UID: NF:shobjidl_core.IFileDialogCustomize.SetControlLabel
title: IFileDialogCustomize::SetControlLabel (shobjidl_core.h)
description: Sets the text associated with a control, such as button text or an edit box label.
helpviewer_keywords: ["IFileDialogCustomize interface [Windows Shell]","SetControlLabel method","IFileDialogCustomize.SetControlLabel","IFileDialogCustomize::SetControlLabel","SetControlLabel","SetControlLabel method [Windows Shell]","SetControlLabel method [Windows Shell]","IFileDialogCustomize interface","shell.IFileDialogCustomize_SetControlLabel","shell_IFileDialogCustomize_SetControlLabel","shobjidl_core/IFileDialogCustomize::SetControlLabel"]
old-location: shell\IFileDialogCustomize_SetControlLabel.htm
tech.root: shell
ms.assetid: 369038ad-999b-425c-bd47-b6a06e5f6939
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetControlLabel method, IFileDialogCustomize.SetControlLabel, IFileDialogCustomize::SetControlLabel, SetControlLabel, SetControlLabel method [Windows Shell], SetControlLabel method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetControlLabel, shell_IFileDialogCustomize_SetControlLabel, shobjidl_core/IFileDialogCustomize::SetControlLabel
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
 - IFileDialogCustomize::SetControlLabel
 - shobjidl_core/IFileDialogCustomize::SetControlLabel
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
 - IFileDialogCustomize.SetControlLabel
---

# IFileDialogCustomize::SetControlLabel


## -description

Sets the text associated with a control, such as button text or an edit box label.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control whose text is to be changed.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the text as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Control labels can be changed at any time, including when the dialog is visible.

