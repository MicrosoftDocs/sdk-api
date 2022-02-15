---
UID: NF:shobjidl_core.IFileDialogCustomize.AddText
title: IFileDialogCustomize::AddText (shobjidl_core.h)
description: Adds text content to the dialog.
helpviewer_keywords: ["AddText","AddText method [Windows Shell]","AddText method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","AddText method","IFileDialogCustomize.AddText","IFileDialogCustomize::AddText","shell.IFileDialogCustomize_AddText","shell_IFileDialogCustomize_AddText","shobjidl_core/IFileDialogCustomize::AddText"]
old-location: shell\IFileDialogCustomize_AddText.htm
tech.root: shell
ms.assetid: efea2fdb-4006-4567-b53c-faa891d18c7e
ms.date: 12/05/2018
ms.keywords: AddText, AddText method [Windows Shell], AddText method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],AddText method, IFileDialogCustomize.AddText, IFileDialogCustomize::AddText, shell.IFileDialogCustomize_AddText, shell_IFileDialogCustomize_AddText, shobjidl_core/IFileDialogCustomize::AddText
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
 - IFileDialogCustomize::AddText
 - shobjidl_core/IFileDialogCustomize::AddText
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
 - IFileDialogCustomize.AddText
---

# IFileDialogCustomize::AddText


## -description

Adds text content to the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the text to add.

### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the text as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default state for this control is enabled and visible.

