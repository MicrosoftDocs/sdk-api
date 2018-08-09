---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreDeleteItem
title: IFileOperationProgressSink::PreDeleteItem
author: windows-sdk-content
description: Performs caller-implemented actions before the delete process for each item begins.
old-location: shell\IFileOperationProgressSink_PreDeleteItem.htm
old-project: shell
ms.assetid: bf54f2da-4861-4546-9b1e-35b5983e836c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreDeleteItem method, IFileOperationProgressSink.PreDeleteItem, IFileOperationProgressSink::PreDeleteItem, PreDeleteItem, PreDeleteItem method [Windows Shell], PreDeleteItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreDeleteItem, shell.IFileOperationProgressSink_PreDeleteItem, shobjidl_core/IFileOperationProgressSink::PreDeleteItem
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
 - IFileOperationProgressSink.PreDeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperationProgressSink::PreDeleteItem


## -description


Performs caller-implemented actions before the delete process for each item begins.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the item to be deleted.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the delete operation and all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



