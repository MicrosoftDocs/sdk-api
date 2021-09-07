---
UID: NF:shobjidl_core.IFileDialog.SetTitle
title: IFileDialog::SetTitle (shobjidl_core.h)
description: Sets the title of the dialog.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetTitle method","IFileDialog.SetTitle","IFileDialog::SetTitle","SetTitle","SetTitle method [Windows Shell]","SetTitle method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetTitle","shell_IFileDialog_SetTitle","shobjidl_core/IFileDialog::SetTitle"]
old-location: shell\IFileDialog_SetTitle.htm
tech.root: shell
ms.assetid: 9ae3d226-e825-443a-a2b0-4b5bb07fc9f7
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetTitle method, IFileDialog.SetTitle, IFileDialog::SetTitle, SetTitle, SetTitle method [Windows Shell], SetTitle method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetTitle, shell_IFileDialog_SetTitle, shobjidl_core/IFileDialog::SetTitle
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
 - IFileDialog::SetTitle
 - shobjidl_core/IFileDialog::SetTitle
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
 - IFileDialog.SetTitle
---

# IFileDialog::SetTitle


## -description

Sets the title of the dialog.

## -parameters

### -param pszTitle [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the title text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

