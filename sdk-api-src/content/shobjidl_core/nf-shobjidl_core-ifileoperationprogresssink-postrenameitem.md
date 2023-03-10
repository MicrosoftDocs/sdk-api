---
UID: NF:shobjidl_core.IFileOperationProgressSink.PostRenameItem
title: IFileOperationProgressSink::PostRenameItem (shobjidl_core.h)
description: Performs caller-implemented actions after the rename process for each item is complete.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PostRenameItem method","IFileOperationProgressSink.PostRenameItem","IFileOperationProgressSink::PostRenameItem","PostRenameItem","PostRenameItem method [Windows Shell]","PostRenameItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PostRenameItem","shell.IFileOperationProgressSink_PostRenameItem","shobjidl_core/IFileOperationProgressSink::PostRenameItem"]
old-location: shell\IFileOperationProgressSink_PostRenameItem.htm
tech.root: shell
ms.assetid: 3bb55ecf-a975-4e7f-9e41-30e778d4cbac
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PostRenameItem method, IFileOperationProgressSink.PostRenameItem, IFileOperationProgressSink::PostRenameItem, PostRenameItem, PostRenameItem method [Windows Shell], PostRenameItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PostRenameItem, shell.IFileOperationProgressSink_PostRenameItem, shobjidl_core/IFileOperationProgressSink::PostRenameItem
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
 - IFileOperationProgressSink::PostRenameItem
 - shobjidl_core/IFileOperationProgressSink::PostRenameItem
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
 - IFileOperationProgressSink.PostRenameItem
---

# IFileOperationProgressSink::PostRenameItem


## -description

Performs caller-implemented actions after the rename process for each item is complete.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that were used during the rename operation. Some values can be set or changed during the rename operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the item before it was renamed.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname">display name</a> of the item. This is a null-terminated, Unicode string. Note that this might not be the name that you asked for, given collisions and other naming rules.

### -param hrRename [in]

Type: <b>HRESULT</b>

The return value of the rename operation. Note that this is not the HRESULT returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">RenameItem</a>, which simply queues the rename operation. Instead, this is the result of the actual rename operation.

### -param psiNewlyCreated [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the item with its new name.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.