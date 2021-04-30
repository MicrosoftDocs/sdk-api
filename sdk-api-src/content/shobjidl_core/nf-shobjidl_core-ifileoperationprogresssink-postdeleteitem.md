---
UID: NF:shobjidl_core.IFileOperationProgressSink.PostDeleteItem
title: IFileOperationProgressSink::PostDeleteItem (shobjidl_core.h)
description: Performs caller-implemented actions after the delete process for each item is complete.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PostDeleteItem method","IFileOperationProgressSink.PostDeleteItem","IFileOperationProgressSink::PostDeleteItem","PostDeleteItem","PostDeleteItem method [Windows Shell]","PostDeleteItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PostDeleteItem","shell.IFileOperationProgressSink_PostDeleteItem","shobjidl_core/IFileOperationProgressSink::PostDeleteItem"]
old-location: shell\IFileOperationProgressSink_PostDeleteItem.htm
tech.root: shell
ms.assetid: 6bd69585-3801-4029-9f60-ab1e6fe5108c
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PostDeleteItem method, IFileOperationProgressSink.PostDeleteItem, IFileOperationProgressSink::PostDeleteItem, PostDeleteItem, PostDeleteItem method [Windows Shell], PostDeleteItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PostDeleteItem, shell.IFileOperationProgressSink_PostDeleteItem, shobjidl_core/IFileOperationProgressSink::PostDeleteItem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOperationProgressSink::PostDeleteItem
 - shobjidl_core/IFileOperationProgressSink::PostDeleteItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperationProgressSink.PostDeleteItem
---

# IFileOperationProgressSink::PostDeleteItem


## -description

Performs caller-implemented actions after the delete process for each item is complete.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that were used during the delete operation. Some values can be set or changed during the delete operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the item that was deleted.

### -param hrDelete [in]

Type: <b>HRESULT</b>

The return value of the delete operation. Note that this is not the HRESULT returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitem">DeleteItem</a>, which simply queues the delete operation. Instead, this is the result of the actual deletion.

### -param psiNewlyCreated [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the deleted item, now in the Recycle Bin. If the item was fully deleted, this value is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.