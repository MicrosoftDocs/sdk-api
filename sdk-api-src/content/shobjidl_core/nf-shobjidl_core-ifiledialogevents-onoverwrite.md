---
UID: NF:shobjidl_core.IFileDialogEvents.OnOverwrite
title: IFileDialogEvents::OnOverwrite (shobjidl_core.h)
description: Called from the save dialog when the user chooses to overwrite a file.
helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnOverwrite method","IFileDialogEvents.OnOverwrite","IFileDialogEvents::OnOverwrite","OnOverwrite","OnOverwrite method [Windows Shell]","OnOverwrite method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnOverwrite","shell_IFileDialogEvents_OnOverwrite","shobjidl_core/IFileDialogEvents::OnOverwrite"]
old-location: shell\IFileDialogEvents_OnOverwrite.htm
tech.root: shell
ms.assetid: 825dcbed-3248-4d2e-bf5f-5d51f8f0529b
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnOverwrite method, IFileDialogEvents.OnOverwrite, IFileDialogEvents::OnOverwrite, OnOverwrite, OnOverwrite method [Windows Shell], OnOverwrite method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnOverwrite, shell_IFileDialogEvents_OnOverwrite, shobjidl_core/IFileDialogEvents::OnOverwrite
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
 - IFileDialogEvents::OnOverwrite
 - shobjidl_core/IFileDialogEvents::OnOverwrite
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
 - IFileDialogEvents.OnOverwrite
---

# IFileDialogEvents::OnOverwrite


## -description

Called from the save dialog when the user chooses to overwrite a file.

## -parameters

### -param pfd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the interface that represents the item that will be overwritten.

### -param pResponse [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response">FDE_OVERWRITE_RESPONSE</a>*</b>

A pointer to a value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response">FDE_OVERWRITE_RESPONSE</a> enumeration indicating the response to the potential overwrite action.

## -returns

Type: <b>HRESULT</b>

The implementer should return E_NOTIMPL if this method is not implemented; S_OK or an appropriate error code otherwise.

## -remarks

The <b>FOS_OVERWRITEPROMPT</b> flag must be set through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions">IFileDialog::SetOptions</a> before this method is called.
