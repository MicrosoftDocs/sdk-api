---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreCopyItem
title: IFileOperationProgressSink::PreCopyItem (shobjidl_core.h)
description: Performs caller-implemented actions before the copy process for each item begins.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PreCopyItem method","IFileOperationProgressSink.PreCopyItem","IFileOperationProgressSink::PreCopyItem","PreCopyItem","PreCopyItem method [Windows Shell]","PreCopyItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PreCopyItem","shell.IFileOperationProgressSink_PreCopyItem","shobjidl_core/IFileOperationProgressSink::PreCopyItem"]
old-location: shell\IFileOperationProgressSink_PreCopyItem.htm
tech.root: shell
ms.assetid: ee436179-197d-49f6-986c-62a1ea930af5
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreCopyItem method, IFileOperationProgressSink.PreCopyItem, IFileOperationProgressSink::PreCopyItem, PreCopyItem, PreCopyItem method [Windows Shell], PreCopyItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreCopyItem, shell.IFileOperationProgressSink_PreCopyItem, shobjidl_core/IFileOperationProgressSink::PreCopyItem
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
 - IFileOperationProgressSink::PreCopyItem
 - shobjidl_core/IFileOperationProgressSink::PreCopyItem
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
 - IFileOperationProgressSink.PreCopyItem
---

# IFileOperationProgressSink::PreCopyItem


## -description

Performs caller-implemented actions before the copy process for each item begins.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the source item.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to contain the copy of the item.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to a new name for the item after it has been copied. This is a null-terminated Unicode string and can be <b>NULL</b>. If <b>NULL</b>, the name of the destination item is the same as the source.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the copy operation and all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.