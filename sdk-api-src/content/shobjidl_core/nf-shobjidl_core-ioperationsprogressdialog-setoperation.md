---
UID: NF:shobjidl_core.IOperationsProgressDialog.SetOperation
title: IOperationsProgressDialog::SetOperation (shobjidl_core.h)
author: windows-sdk-content
description: Sets which progress dialog operation is occurring, and whether we are in pre-flight or undo mode.
old-location: shell\IOperationsProgressDialog_SetOperation.htm
tech.root: shell
ms.assetid: b6fae1df-1c27-4ce9-a7f6-c5488f080ef3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOperationsProgressDialog interface [Windows Shell],SetOperation method, IOperationsProgressDialog.SetOperation, IOperationsProgressDialog::SetOperation, SetOperation, SetOperation method [Windows Shell], SetOperation method [Windows Shell],IOperationsProgressDialog interface, _shell_IOperationsProgressDialog_SetOperation, shell.IOperationsProgressDialog_SetOperation, shobjidl_core/IOperationsProgressDialog::SetOperation
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOperationsProgressDialog.SetOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOperationsProgressDialog::SetOperation


## -description


Sets which progress dialog operation is occurring, and whether we are in pre-flight or undo mode.


## -parameters




### -param action [in]

Type: <b><a href="https://msdn.microsoft.com/fc5a0f96-e8c2-483f-86b0-d8c870a9f77a">SPACTION</a></b>

Specifies operation. See <a href="https://msdn.microsoft.com/fc5a0f96-e8c2-483f-86b0-d8c870a9f77a">SPACTION</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



