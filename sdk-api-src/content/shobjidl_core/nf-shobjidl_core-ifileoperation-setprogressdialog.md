---
UID: NF:shobjidl_core.IFileOperation.SetProgressDialog
title: IFileOperation::SetProgressDialog (shobjidl_core.h)
description: Specifies a dialog box used to display the progress of the operation.
helpviewer_keywords: ["IFileOperation interface [Windows Shell]","SetProgressDialog method","IFileOperation.SetProgressDialog","IFileOperation::SetProgressDialog","SetProgressDialog","SetProgressDialog method [Windows Shell]","SetProgressDialog method [Windows Shell]","IFileOperation interface","_shell_IFileOperation_SetProgressDialog","shell.IFileOperation_SetProgressDialog","shobjidl_core/IFileOperation::SetProgressDialog"]
old-location: shell\IFileOperation_SetProgressDialog.htm
tech.root: shell
ms.assetid: 34cc6b88-9791-4778-a8d9-cf1b80aa42a8
ms.date: 12/05/2018
ms.keywords: IFileOperation interface [Windows Shell],SetProgressDialog method, IFileOperation.SetProgressDialog, IFileOperation::SetProgressDialog, SetProgressDialog, SetProgressDialog method [Windows Shell], SetProgressDialog method [Windows Shell],IFileOperation interface, _shell_IFileOperation_SetProgressDialog, shell.IFileOperation_SetProgressDialog, shobjidl_core/IFileOperation::SetProgressDialog
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
 - IFileOperation::SetProgressDialog
 - shobjidl_core/IFileOperation::SetProgressDialog
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
 - IFileOperation.SetProgressDialog
---

# IFileOperation::SetProgressDialog


## -description

Specifies a dialog box used to display the progress of the operation.

## -parameters

### -param popd [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog">IOperationsProgressDialog</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog">IOperationsProgressDialog</a> object that represents the dialog box.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.