---
UID: NF:shobjidl_core.IFileOperationProgressSink.PostCopyItem
title: IFileOperationProgressSink::PostCopyItem (shobjidl_core.h)
description: Performs caller-implemented actions after the copy process for each item is complete.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PostCopyItem method","IFileOperationProgressSink.PostCopyItem","IFileOperationProgressSink::PostCopyItem","PostCopyItem","PostCopyItem method [Windows Shell]","PostCopyItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PostCopyItem","shell.IFileOperationProgressSink_PostCopyItem","shobjidl_core/IFileOperationProgressSink::PostCopyItem"]
old-location: shell\IFileOperationProgressSink_PostCopyItem.htm
tech.root: shell
ms.assetid: 2e5568a8-e689-48ca-82a1-36292d91a65b
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PostCopyItem method, IFileOperationProgressSink.PostCopyItem, IFileOperationProgressSink::PostCopyItem, PostCopyItem, PostCopyItem method [Windows Shell], PostCopyItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PostCopyItem, shell.IFileOperationProgressSink_PostCopyItem, shobjidl_core/IFileOperationProgressSink::PostCopyItem
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
 - IFileOperationProgressSink::PostCopyItem
 - shobjidl_core/IFileOperationProgressSink::PostCopyItem
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
 - IFileOperationProgressSink.PostCopyItem
---

# IFileOperationProgressSink::PostCopyItem


## -description

Performs caller-implemented actions after the copy process for each item is complete.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that were used during the copy operation. Some values can be set or changed during the copy operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the source item.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder to which the item was copied.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the new name that was given to the item after it was copied. This is a null-terminated Unicode string. Note that this might not be the name that you asked for, given collisions and other naming rules.

### -param hrCopy [in]

Type: <b>HRESULT</b>

The return value of the copy operation. Note that this is not the HRESULT returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">CopyItem</a>, which simply queues the copy operation. Instead, this is the result of the actual copy.

### -param psiNewlyCreated [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the new copy of the item.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">CopyItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink">IFileOperationProgressSink</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperationprogresssink-precopyitem">IFileOperationProgressSink::PreCopyItem</a>