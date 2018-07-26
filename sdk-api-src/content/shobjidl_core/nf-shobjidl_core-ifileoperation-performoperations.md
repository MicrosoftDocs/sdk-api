---
UID: NF:shobjidl_core.IFileOperation.PerformOperations
title: IFileOperation::PerformOperations
author: windows-sdk-content
description: Executes all selected operations.
old-location: shell\IFileOperation_PerformOperations.htm
old-project: shell
ms.assetid: eceb5f0a-ad9a-4b7a-9656-c10e0420a96a
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IFileOperation interface [Windows Shell],PerformOperations method, IFileOperation.PerformOperations, IFileOperation::PerformOperations, PerformOperations, PerformOperations method [Windows Shell], PerformOperations method [Windows Shell],IFileOperation interface, _shell_IFileOperation_PerformOperations, shell.IFileOperation_PerformOperations, shobjidl_core/IFileOperation::PerformOperations
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
 - IFileOperation.PerformOperations
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::PerformOperations


## -description


Executes all selected operations.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Note that if the operation was canceled by the user, this method can still return a success code. Use the <a href="https://msdn.microsoft.com/988f78a8-3a50-44d8-9214-7cf71be72d38">GetAnyOperationsAborted</a> method to determine if this was the case.




## -remarks



This method is called last to execute those actions that have been specified earlier by calling their individual methods. For instance, <a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">RenameItem</a> does not rename the item, it simply sets the parameters. The actual renaming is done when you call <b>PerformOperations</b>.




## -see-also




<a href="https://msdn.microsoft.com/5d2d05c3-525d-4113-bb08-63395facf191">FinishOperations</a>



<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/8b9e4423-ead7-44be-b960-5ee83025f42a">StartOperations</a>
 

 

