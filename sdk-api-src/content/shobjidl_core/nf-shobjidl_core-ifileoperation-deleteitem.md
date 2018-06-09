---
UID: NF:shobjidl_core.IFileOperation.DeleteItem
title: IFileOperation::DeleteItem
author: windows-sdk-content
description: Declares a single item that is to be deleted.
old-location: shell\IFileOperation_DeleteItem.htm
old-project: shell
ms.assetid: 177ce480-0309-4ec8-a6f2-0be9196bd2c8
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DeleteItem, DeleteItem method [Windows Shell], DeleteItem method [Windows Shell],IFileOperation interface, IFileOperation interface [Windows Shell],DeleteItem method, IFileOperation.DeleteItem, IFileOperation::DeleteItem, _shell_IFileOperation_DeleteItem, shell.IFileOperation_DeleteItem, shobjidl_core/IFileOperation::DeleteItem
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
 - IFileOperation.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::DeleteItem


## -description


Declares a single item that is to be deleted.


## -parameters




### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the item to be deleted.


### -param pfopsItem [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object to be used for progress status and error notifications for this specific delete operation. If you call <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the delete operation are included there, so set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not delete the item, it merely declares the item to be deleted. To delete an item, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::DeleteItem</b> to declare the file or folder to be deleted.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the delete operation.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/708072c4-c0c7-4d7d-a54f-234c57ff08e6">IFileOperation::DeleteItems</a>



<a href="https://msdn.microsoft.com/6bd69585-3801-4029-9f60-ab1e6fe5108c">PostDeleteItem</a>



<a href="https://msdn.microsoft.com/bf54f2da-4861-4546-9b1e-35b5983e836c">PreDeleteItem</a>
 

 

