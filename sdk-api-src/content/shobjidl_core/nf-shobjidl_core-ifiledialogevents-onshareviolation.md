---
UID: NF:shobjidl_core.IFileDialogEvents.OnShareViolation
title: IFileDialogEvents::OnShareViolation (shobjidl_core.h)
description: Enables an application to respond to sharing violations that arise from Open or Save operations.
helpviewer_keywords: ["IFileDialogEvents interface [Windows Shell]","OnShareViolation method","IFileDialogEvents.OnShareViolation","IFileDialogEvents::OnShareViolation","OnShareViolation","OnShareViolation method [Windows Shell]","OnShareViolation method [Windows Shell]","IFileDialogEvents interface","shell.IFileDialogEvents_OnShareViolation","shell_IFileDialogEvents_OnShareViolation","shobjidl_core/IFileDialogEvents::OnShareViolation"]
old-location: shell\IFileDialogEvents_OnShareViolation.htm
tech.root: shell
ms.assetid: bd9cfa69-4e55-48ca-915a-e5ecccf8bf96
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnShareViolation method, IFileDialogEvents.OnShareViolation, IFileDialogEvents::OnShareViolation, OnShareViolation, OnShareViolation method [Windows Shell], OnShareViolation method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnShareViolation, shell_IFileDialogEvents_OnShareViolation, shobjidl_core/IFileDialogEvents::OnShareViolation
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
 - IFileDialogEvents::OnShareViolation
 - shobjidl_core/IFileDialogEvents::OnShareViolation
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
 - IFileDialogEvents.OnShareViolation
---

# IFileDialogEvents::OnShareViolation


## -description

Enables an application to respond to sharing violations that arise from Open or Save operations.

## -parameters

### -param pfd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the interface that represents the item that has the sharing violation.

### -param pResponse [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response">FDE_SHAREVIOLATION_RESPONSE</a>*</b>

A pointer to a value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response">FDE_SHAREVIOLATION_RESPONSE</a> enumeration indicating the response to the sharing violation.

## -returns

Type: <b>HRESULT</b>

The implementer should return E_NOTIMPL if this method is not implemented; S_OK or an appropriate error code otherwise.

## -remarks

The <b>FOS_SHAREAWARE</b> flag must be set through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions">IFileDialog::SetOptions</a> before this method is called.

A sharing violation could possibly arise when the application attempts to open a file, because the file could have been locked between the time that the dialog tested it and the application opened it.