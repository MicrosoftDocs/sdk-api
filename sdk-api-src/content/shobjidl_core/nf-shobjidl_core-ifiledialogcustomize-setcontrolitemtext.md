---
UID: NF:shobjidl_core.IFileDialogCustomize.SetControlItemText
title: IFileDialogCustomize::SetControlItemText (shobjidl_core.h)
description: Sets the text of a control item. For example, the text that accompanies a radio button or an item in a menu.
helpviewer_keywords: ["IFileDialogCustomize interface [Windows Shell]","SetControlItemText method","IFileDialogCustomize.SetControlItemText","IFileDialogCustomize::SetControlItemText","SetControlItemText","SetControlItemText method [Windows Shell]","SetControlItemText method [Windows Shell]","IFileDialogCustomize interface","shell.IFileDialogCustomize_SetControlItemText","shell_IFileDialogCustomize_SetControlItemText","shobjidl_core/IFileDialogCustomize::SetControlItemText"]
old-location: shell\IFileDialogCustomize_SetControlItemText.htm
tech.root: shell
ms.assetid: d89f67ee-ff56-4810-9627-e8f35e653ff4
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetControlItemText method, IFileDialogCustomize.SetControlItemText, IFileDialogCustomize::SetControlItemText, SetControlItemText, SetControlItemText method [Windows Shell], SetControlItemText method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetControlItemText, shell_IFileDialogCustomize_SetControlItemText, shobjidl_core/IFileDialogCustomize::SetControlItemText
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
 - IFileDialogCustomize::SetControlItemText
 - shobjidl_core/IFileDialogCustomize::SetControlItemText
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
 - IFileDialogCustomize.SetControlItemText
---

# IFileDialogCustomize::SetControlItemText


## -description

Sets the text of a control item. For example, the text that accompanies a radio button or an item in a menu.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the container control.

### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the item.

### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated buffer that contains a Unicode string with the text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state of a control item is enabled and visible. Items in control groups cannot be changed after they have been created, with the exception of their enabled and visible states.

Container controls include option button groups, combo boxes, drop-down lists on the <b>Open</b> or <b>Save</b> button, and menus.

