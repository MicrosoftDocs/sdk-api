---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreNewItem
title: IFileOperationProgressSink::PreNewItem (shobjidl_core.h)
description: Performs caller-implemented actions before the process to create a new item begins.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PreNewItem method","IFileOperationProgressSink.PreNewItem","IFileOperationProgressSink::PreNewItem","PreNewItem","PreNewItem method [Windows Shell]","PreNewItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PreNewItem","shell.IFileOperationProgressSink_PreNewItem","shobjidl_core/IFileOperationProgressSink::PreNewItem"]
old-location: shell\IFileOperationProgressSink_PreNewItem.htm
tech.root: shell
ms.assetid: ea6223e1-a574-4e4b-a264-384f33579c6d
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreNewItem method, IFileOperationProgressSink.PreNewItem, IFileOperationProgressSink::PreNewItem, PreNewItem, PreNewItem method [Windows Shell], PreNewItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreNewItem, shell.IFileOperationProgressSink_PreNewItem, shobjidl_core/IFileOperationProgressSink::PreNewItem
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
 - IFileOperationProgressSink::PreNewItem
 - shobjidl_core/IFileOperationProgressSink::PreNewItem
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
 - IFileOperationProgressSink.PreNewItem
---

# IFileOperationProgressSink::PreNewItem


## -description

Performs caller-implemented actions before the process to create a new item begins.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiDestinationFolder [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the destination folder that will contain the new item.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

Pointer to the file name of the new item, for instance <b>Newfile.txt</b>. This is a null-terminated, Unicode string.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, this operation and all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.