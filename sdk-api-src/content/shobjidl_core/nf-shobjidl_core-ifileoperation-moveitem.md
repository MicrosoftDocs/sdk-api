---
UID: NF:shobjidl_core.IFileOperation.MoveItem
title: IFileOperation::MoveItem
author: windows-sdk-content
description: Declares a single item that is to be moved to a specified destination.
old-location: shell\IFileOperation_MoveItem.htm
old-project: shell
ms.assetid: 7b1e66c9-5264-42cb-9554-d1ea92625c6f
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IFileOperation interface [Windows Shell],MoveItem method, IFileOperation.MoveItem, IFileOperation::MoveItem, MoveItem, MoveItem method [Windows Shell], MoveItem method [Windows Shell],IFileOperation interface, _shell_IFileOperation_MoveItem, shell.IFileOperation_MoveItem, shobjidl_core/IFileOperation::MoveItem
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
 - IFileOperation.MoveItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::MoveItem


## -description


Declares a single item that is to be moved to a specified destination.


## -parameters




### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the source item.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to contain the moved item.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item in its new location. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.


### -param pfopsItem [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object to be used for progress status and error notifications for this specific move operation. If you call <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the move operation are included there, so set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not move the item, it merely declares the item to be moved. To move an object, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::MoveItem</b> to declare the source item, destination folder, and destination name.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the move operation.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/7b3c3fc9-5e08-44be-b0ba-a67702e2deb6">IFileOperation::MoveItems</a>



<a href="https://msdn.microsoft.com/cd353e15-4b1c-4d02-aa3f-c8d744a1722f">PostMoveItem</a>



<a href="https://msdn.microsoft.com/bd92c9fa-fdea-4149-9727-90eafdf7c6bc">PreMoveItem</a>
 

 

