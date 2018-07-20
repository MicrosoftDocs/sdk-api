---
UID: NF:shobjidl_core.IFileOperationProgressSink.FinishOperations
title: IFileOperationProgressSink::FinishOperations
author: windows-sdk-content
description: Performs caller-implemented actions after the last operation performed by the call to IFileOperation is complete.
old-location: shell\IFileOperationProgressSink_FinishOperations.htm
old-project: shell
ms.assetid: 5d2d05c3-525d-4113-bb08-63395facf191
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FinishOperations, FinishOperations method [Windows Shell], FinishOperations method [Windows Shell],IFileOperationProgressSink interface, IFileOperationProgressSink interface [Windows Shell],FinishOperations method, IFileOperationProgressSink.FinishOperations, IFileOperationProgressSink::FinishOperations, _shell_IFileOperationProgressSink_FinishOperations, shell.IFileOperationProgressSink_FinishOperations, shobjidl_core/IFileOperationProgressSink::FinishOperations
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
 - IFileOperationProgressSink.FinishOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperationProgressSink::FinishOperations


## -description


Performs caller-implemented actions after the last operation performed by the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> is complete.


## -parameters




### -param hrResult [in]

Type: <b>HRESULT</b>

The return value of the final operation. Note that this is not the HRESULT returned by one of the <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> methods, which simply queue the operations. Instead, this is the result of the actual operation, such as copy, delete, or move.


## -returns



Type: <b>HRESULT</b>

Not used.



