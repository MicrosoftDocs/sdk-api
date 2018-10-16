---
UID: NF:shobjidl_core.IFileOperationProgressSink.PostMoveItem
title: IFileOperationProgressSink::PostMoveItem
author: windows-sdk-content
description: Performs caller-implemented actions after the move process for each item is complete.
old-location: shell\IFileOperationProgressSink_PostMoveItem.htm
tech.root: shell
ms.assetid: cd353e15-4b1c-4d02-aa3f-c8d744a1722f
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PostMoveItem method, IFileOperationProgressSink.PostMoveItem, IFileOperationProgressSink::PostMoveItem, PostMoveItem, PostMoveItem method [Windows Shell], PostMoveItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PostMoveItem, shell.IFileOperationProgressSink_PostMoveItem, shobjidl_core/IFileOperationProgressSink::PostMoveItem
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
 - IFileOperationProgressSink.PostMoveItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink::PostMoveItem


## -description


Performs caller-implemented actions after the move process for each item is complete.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that were used during the move operation. Some values can be set or changed during the move operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the source item.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder that contains the moved item.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the name that was given to the item after it was moved. This is a null-terminated Unicode string. Note that this might not be the name that you asked for, given collisions and other naming rules.


### -param hrMove [in]

Type: <b>HRESULT</b>

The return value of the move operation. Note that this is not the HRESULT returned by <a href="https://msdn.microsoft.com/7b1e66c9-5264-42cb-9554-d1ea92625c6f">MoveItem</a>, which simply queues the move operation. Instead, this is the result of the actual move.


### -param psiNewlyCreated [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the moved item in its new location.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



