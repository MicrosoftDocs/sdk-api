---
UID: NF:shobjidl_core.IOperationsProgressDialog.GetOperationStatus
title: IOperationsProgressDialog::GetOperationStatus (shobjidl_core.h)
description: Gets operation status for progress dialog.
helpviewer_keywords: ["GetOperationStatus","GetOperationStatus method [Windows Shell]","GetOperationStatus method [Windows Shell]","IOperationsProgressDialog interface","IOperationsProgressDialog interface [Windows Shell]","GetOperationStatus method","IOperationsProgressDialog.GetOperationStatus","IOperationsProgressDialog::GetOperationStatus","_shell_IOperationsProgressDialog_GetOperationStatus","shell.IOperationsProgressDialog_GetOperationStatus","shobjidl_core/IOperationsProgressDialog::GetOperationStatus"]
old-location: shell\IOperationsProgressDialog_GetOperationStatus.htm
tech.root: shell
ms.assetid: bd796369-9789-4c69-b699-eb0ec0e571b2
ms.date: 12/05/2018
ms.keywords: GetOperationStatus, GetOperationStatus method [Windows Shell], GetOperationStatus method [Windows Shell],IOperationsProgressDialog interface, IOperationsProgressDialog interface [Windows Shell],GetOperationStatus method, IOperationsProgressDialog.GetOperationStatus, IOperationsProgressDialog::GetOperationStatus, _shell_IOperationsProgressDialog_GetOperationStatus, shell.IOperationsProgressDialog_GetOperationStatus, shobjidl_core/IOperationsProgressDialog::GetOperationStatus
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
 - IOperationsProgressDialog::GetOperationStatus
 - shobjidl_core/IOperationsProgressDialog::GetOperationStatus
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
 - IOperationsProgressDialog.GetOperationStatus
---

# IOperationsProgressDialog::GetOperationStatus


## -description

Gets operation status for progress dialog.

## -parameters

### -param popstatus [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-pdopstatus">PDOPSTATUS</a>*</b>

Contains pointer to the operation status. See <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-pdopstatus">PDOPSTATUS</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.