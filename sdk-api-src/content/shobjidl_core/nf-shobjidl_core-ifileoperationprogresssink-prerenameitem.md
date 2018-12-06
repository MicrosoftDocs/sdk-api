---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreRenameItem
title: IFileOperationProgressSink::PreRenameItem
author: windows-sdk-content
description: Performs caller-implemented actions before the rename process for each item begins.
old-location: shell\IFileOperationProgressSink_PreRenameItem.htm
tech.root: shell
ms.assetid: 444fe15b-cbed-46d8-ae25-ab6a569d18e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreRenameItem method, IFileOperationProgressSink.PreRenameItem, IFileOperationProgressSink::PreRenameItem, PreRenameItem, PreRenameItem method [Windows Shell], PreRenameItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreRenameItem, shell.IFileOperationProgressSink_PreRenameItem, shobjidl_core/IFileOperationProgressSink::PreRenameItem
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
 - IFileOperationProgressSink.PreRenameItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink::PreRenameItem


## -description


Performs caller-implemented actions before the rename process for each item begins.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the item to be renamed.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new <a href="https://msdn.microsoft.com/9b159be9-3797-4c8b-90f8-9d3b3a3afb71">display name</a> of the item. This is a null-terminated, Unicode string.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the rename operation and all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



