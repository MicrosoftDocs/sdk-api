---
UID: NF:shobjidl_core.IFileOperation.RenameItem
title: IFileOperation::RenameItem
author: windows-sdk-content
description: Declares a single item that is to be given a new display name.
old-location: shell\IFileOperation_RenameItem.htm
old-project: shell
ms.assetid: 2f72b729-3535-4ab7-9579-21b1ba97c67f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IFileOperation interface [Windows Shell],RenameItem method, IFileOperation.RenameItem, IFileOperation::RenameItem, RenameItem, RenameItem method [Windows Shell], RenameItem method [Windows Shell],IFileOperation interface, _shell_IFileOperation_RenameItem, shell.IFileOperation_RenameItem, shobjidl_core/IFileOperation::RenameItem
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
 - IFileOperation.RenameItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::RenameItem


## -description


Declares a single item that is to be given a new display name.


## -parameters




### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the source item.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new <a href="https://msdn.microsoft.com/9b159be9-3797-4c8b-90f8-9d3b3a3afb71">display name</a> of the item. This is a null-terminated, Unicode string.


### -param pfopsItem [in]

Type: <b><a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a> object to be used for status and failure notifications. If you call <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> for the overall operation, progress status and error notifications for the rename operation are included there, so set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not rename the item, it merely declares the item to be renamed. To rename an object, you must make at least the sequence of calls detailed here:
                

<ol>
<li>Call <b>IFileOperation::RenameItem</b> to declare the new name.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to begin the rename operation.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/325c09c6-ae32-4f5d-8b21-174dafc94aea">IFileOperation::RenameItems</a>



<a href="https://msdn.microsoft.com/3bb55ecf-a975-4e7f-9e41-30e778d4cbac">PostRenameItem</a>



<a href="https://msdn.microsoft.com/444fe15b-cbed-46d8-ae25-ab6a569d18e0">PreRenameItem</a>
 

 

