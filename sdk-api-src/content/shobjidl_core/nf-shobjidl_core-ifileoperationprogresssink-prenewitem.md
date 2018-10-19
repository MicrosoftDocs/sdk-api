---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreNewItem
title: IFileOperationProgressSink::PreNewItem
author: windows-sdk-content
description: Performs caller-implemented actions before the process to create a new item begins.
old-location: shell\IFileOperationProgressSink_PreNewItem.htm
tech.root: shell
ms.assetid: ea6223e1-a574-4e4b-a264-384f33579c6d
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreNewItem method, IFileOperationProgressSink.PreNewItem, IFileOperationProgressSink::PreNewItem, PreNewItem, PreNewItem method [Windows Shell], PreNewItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreNewItem, shell.IFileOperationProgressSink_PreNewItem, shobjidl_core/IFileOperationProgressSink::PreNewItem
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
 - IFileOperationProgressSink.PreNewItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink::PreNewItem


## -description


Performs caller-implemented actions before the process to create a new item begins.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="https://msdn.microsoft.com/8a3da00a-1d96-444d-acbe-9327620b8d24">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.


### -param psiDestinationFolder [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that specifies the destination folder that will contain the new item.


### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the file name of the new item, for instance <b>Newfile.txt</b>. This is a null-terminated, Unicode string.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, this operation and all subsequent operations pending from the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> are canceled.



