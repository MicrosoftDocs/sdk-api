---
UID: NF:shobjidl_core.IOperationsProgressDialog.GetMilliseconds
title: IOperationsProgressDialog::GetMilliseconds
author: windows-sdk-content
description: Gets elapsed and remaining time for progress dialog.
old-location: shell\IOperationsProgressDialog_GetMilliseconds.htm
old-project: shell
ms.assetid: 0e1c34cf-1fa2-43b7-91c9-2ec9224b5b39
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: GetMilliseconds, GetMilliseconds method [Windows Shell], GetMilliseconds method [Windows Shell],IOperationsProgressDialog interface, IOperationsProgressDialog interface [Windows Shell],GetMilliseconds method, IOperationsProgressDialog.GetMilliseconds, IOperationsProgressDialog::GetMilliseconds, _shell_IOperationsProgressDialog_GetMilliseconds, shell.IOperationsProgressDialog_GetMilliseconds, shobjidl_core/IOperationsProgressDialog::GetMilliseconds
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
 - IOperationsProgressDialog.GetMilliseconds
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IOperationsProgressDialog::GetMilliseconds


## -description


Gets elapsed and remaining time for progress dialog.


## -parameters




### -param pullElapsed [out]

Type: <b>ULONGLONG*</b>

A pointer to the elapsed time in milliseconds.


### -param pullRemaining [out]

Type: <b>ULONGLONG*</b>

A pointer to the remaining time in milliseconds.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



