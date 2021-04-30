---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreMoveItem
title: IFileOperationProgressSink::PreMoveItem (shobjidl_core.h)
description: Performs caller-implemented actions before the move process for each item begins.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PreMoveItem method","IFileOperationProgressSink.PreMoveItem","IFileOperationProgressSink::PreMoveItem","PreMoveItem","PreMoveItem method [Windows Shell]","PreMoveItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PreMoveItem","shell.IFileOperationProgressSink_PreMoveItem","shobjidl_core/IFileOperationProgressSink::PreMoveItem"]
old-location: shell\IFileOperationProgressSink_PreMoveItem.htm
tech.root: shell
ms.assetid: bd92c9fa-fdea-4149-9727-90eafdf7c6bc
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreMoveItem method, IFileOperationProgressSink.PreMoveItem, IFileOperationProgressSink::PreMoveItem, PreMoveItem, PreMoveItem method [Windows Shell], PreMoveItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreMoveItem, shell.IFileOperationProgressSink_PreMoveItem, shobjidl_core/IFileOperationProgressSink::PreMoveItem
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
 - IFileOperationProgressSink::PreMoveItem
 - shobjidl_core/IFileOperationProgressSink::PreMoveItem
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
 - IFileOperationProgressSink.PreMoveItem
---

# IFileOperationProgressSink::PreMoveItem


## -description

Performs caller-implemented actions before the move process for each item begins.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the item to be moved.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to contain the moved item.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item in its new location. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the move operation and all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.