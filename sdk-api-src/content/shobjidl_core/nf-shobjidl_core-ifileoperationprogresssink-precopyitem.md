---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreCopyItem
title: IFileOperationProgressSink::PreCopyItem
author: windows-driver-content
description: Performs caller-implemented actions before the copy process for each item begins.
old-location: shell\IFileOperationProgressSink_PreCopyItem.htm
old-project: shell
ms.assetid: ee436179-197d-49f6-986c-62a1ea930af5
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreCopyItem method, IFileOperationProgressSink.PreCopyItem, IFileOperationProgressSink::PreCopyItem, PreCopyItem, PreCopyItem method [Windows Shell], PreCopyItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreCopyItem, shell.IFileOperationProgressSink_PreCopyItem, shobjidl_core/IFileOperationProgressSink::PreCopyItem
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileOperationProgressSink.PreCopyItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperationProgressSink::PreCopyItem


## -description


Performs caller-implemented actions before the copy process for each item begins.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the source item.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder to contain the copy of the item.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item after it has been copied. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the copy operation and all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



