---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreMoveItem
title: IFileOperationProgressSink::PreMoveItem
author: windows-sdk-content
description: Performs caller-implemented actions before the move process for each item begins.
old-location: shell\IFileOperationProgressSink_PreMoveItem.htm
tech.root: shell
ms.assetid: bd92c9fa-fdea-4149-9727-90eafdf7c6bc
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreMoveItem method, IFileOperationProgressSink.PreMoveItem, IFileOperationProgressSink::PreMoveItem, PreMoveItem, PreMoveItem method [Windows Shell], PreMoveItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreMoveItem, shell.IFileOperationProgressSink_PreMoveItem, shobjidl_core/IFileOperationProgressSink::PreMoveItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFileOperationProgressSink.PreMoveItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink::PreMoveItem


## -description


Performs caller-implemented actions before the move process for each item begins.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the item to be moved.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to contain the moved item.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item in its new location. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the move operation and all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



