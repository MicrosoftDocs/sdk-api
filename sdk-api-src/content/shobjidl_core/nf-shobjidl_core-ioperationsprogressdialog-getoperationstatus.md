---
UID: NF:shobjidl_core.IOperationsProgressDialog.GetOperationStatus
title: IOperationsProgressDialog::GetOperationStatus
author: windows-sdk-content
description: Gets operation status for progress dialog.
old-location: shell\IOperationsProgressDialog_GetOperationStatus.htm
old-project: shell
ms.assetid: bd796369-9789-4c69-b699-eb0ec0e571b2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetOperationStatus, GetOperationStatus method [Windows Shell], GetOperationStatus method [Windows Shell],IOperationsProgressDialog interface, IOperationsProgressDialog interface [Windows Shell],GetOperationStatus method, IOperationsProgressDialog.GetOperationStatus, IOperationsProgressDialog::GetOperationStatus, _shell_IOperationsProgressDialog_GetOperationStatus, shell.IOperationsProgressDialog_GetOperationStatus, shobjidl_core/IOperationsProgressDialog::GetOperationStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOperationsProgressDialog.GetOperationStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IOperationsProgressDialog::GetOperationStatus


## -description


Gets operation status for progress dialog.


## -parameters




### -param popstatus [out]

Type: <b><a href="https://msdn.microsoft.com/f9fd5cbe-2cb7-4ae7-9cf2-f8545095eec8">PDOPSTATUS</a>*</b>

Contains pointer to the operation status. See <a href="https://msdn.microsoft.com/f9fd5cbe-2cb7-4ae7-9cf2-f8545095eec8">PDOPSTATUS</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



