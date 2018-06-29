---
UID: NF:shobjidl_core.IFileOperationProgressSink.PostCopyItem
title: IFileOperationProgressSink::PostCopyItem
author: windows-sdk-content
description: Performs caller-implemented actions after the copy process for each item is complete.
old-location: shell\IFileOperationProgressSink_PostCopyItem.htm
old-project: shell
ms.assetid: 2e5568a8-e689-48ca-82a1-36292d91a65b
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PostCopyItem method, IFileOperationProgressSink.PostCopyItem, IFileOperationProgressSink::PostCopyItem, PostCopyItem, PostCopyItem method [Windows Shell], PostCopyItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PostCopyItem, shell.IFileOperationProgressSink_PostCopyItem, shobjidl_core/IFileOperationProgressSink::PostCopyItem
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
 - IFileOperationProgressSink.PostCopyItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperationProgressSink::PostCopyItem


## -description


Performs caller-implemented actions after the copy process for each item is complete.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that were used during the copy operation. Some values can be set or changed during the copy operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the source item.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to which the item was copied.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new name that was given to the item after it was copied. This is a null-terminated Unicode string. Note that this might not be the name that you asked for, given collisions and other naming rules.


### -param hrCopy [in]

Type: <b>HRESULT</b>

The return value of the copy operation. Note that this is not the HRESULT returned by <a href="https://msdn.microsoft.com/36d623b7-67c3-48b7-be9b-9264b5b8d919">CopyItem</a>, which simply queues the copy operation. Instead, this is the result of the actual copy.


### -param psiNewlyCreated [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the new copy of the item.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.




## -see-also




<a href="https://msdn.microsoft.com/36d623b7-67c3-48b7-be9b-9264b5b8d919">CopyItem</a>



<a href="https://msdn.microsoft.com/24b20e05-d8be-4060-a966-7b32d9225403">IFileOperationProgressSink</a>



<a href="https://msdn.microsoft.com/ee436179-197d-49f6-986c-62a1ea930af5">IFileOperationProgressSink::PreCopyItem</a>
 

 

