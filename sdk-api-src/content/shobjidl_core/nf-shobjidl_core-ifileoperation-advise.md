---
UID: NF:shobjidl_core.IFileOperation.Advise
title: IFileOperation::Advise
author: windows-sdk-content
description: Enables a handler to provide status and error information for all operations.
old-location: shell\IFileOperation_Advise.htm
old-project: shell
ms.assetid: 458c24b0-9288-4ed7-9a4b-7534f26dd32e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],Advise method, IFileOperation.Advise, IFileOperation::Advise, _shell_IFileOperation_Advise, shell.IFileOperation_Advise, shobjidl_core/IFileOperation::Advise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IFileOperation.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::Advise


## -description


Enables a handler to provide status and error information for all operations.


## -parameters




### -param pfops [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object to be used for progress status and error notifications.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

When this method returns, this parameter points to a returned token that uniquely identifies this connection. The calling application uses this token later to delete the connection by passing it to <a href="https://msdn.microsoft.com/684b3e94-50b9-465e-b4c3-b244fc7209f5">IFileOperation::Unadvise</a>. If the call to <b>Advise</b> fails, this value is meaningless.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Several individual methods have the ability to declare their own progress sinks, which are redundant to the one set here. They are used when you only want to be given progress and error information for a specific operation.




## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/684b3e94-50b9-465e-b4c3-b244fc7209f5">IFileOperation::Unadvise</a>
 

 

