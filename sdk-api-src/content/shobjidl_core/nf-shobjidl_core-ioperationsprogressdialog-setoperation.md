---
UID: NF:shobjidl_core.IOperationsProgressDialog.SetOperation
title: IOperationsProgressDialog::SetOperation (shobjidl_core.h)
description: Sets which progress dialog operation is occurring, and whether we are in pre-flight or undo mode.
helpviewer_keywords: ["IOperationsProgressDialog interface [Windows Shell]","SetOperation method","IOperationsProgressDialog.SetOperation","IOperationsProgressDialog::SetOperation","SetOperation","SetOperation method [Windows Shell]","SetOperation method [Windows Shell]","IOperationsProgressDialog interface","_shell_IOperationsProgressDialog_SetOperation","shell.IOperationsProgressDialog_SetOperation","shobjidl_core/IOperationsProgressDialog::SetOperation"]
old-location: shell\IOperationsProgressDialog_SetOperation.htm
tech.root: shell
ms.assetid: b6fae1df-1c27-4ce9-a7f6-c5488f080ef3
ms.date: 12/05/2018
ms.keywords: IOperationsProgressDialog interface [Windows Shell],SetOperation method, IOperationsProgressDialog.SetOperation, IOperationsProgressDialog::SetOperation, SetOperation, SetOperation method [Windows Shell], SetOperation method [Windows Shell],IOperationsProgressDialog interface, _shell_IOperationsProgressDialog_SetOperation, shell.IOperationsProgressDialog_SetOperation, shobjidl_core/IOperationsProgressDialog::SetOperation
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
 - IOperationsProgressDialog::SetOperation
 - shobjidl_core/IOperationsProgressDialog::SetOperation
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
 - IOperationsProgressDialog.SetOperation
---

# IOperationsProgressDialog::SetOperation


## -description

Sets which progress dialog operation is occurring, and whether we are in pre-flight or undo mode.

## -parameters

### -param action [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction">SPACTION</a></b>

Specifies operation. See <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction">SPACTION</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.