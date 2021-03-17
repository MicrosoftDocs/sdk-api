---
UID: NF:shobjidl_core.IFileOperationProgressSink.PreDeleteItem
title: IFileOperationProgressSink::PreDeleteItem (shobjidl_core.h)
description: Performs caller-implemented actions before the delete process for each item begins.
helpviewer_keywords: ["IFileOperationProgressSink interface [Windows Shell]","PreDeleteItem method","IFileOperationProgressSink.PreDeleteItem","IFileOperationProgressSink::PreDeleteItem","PreDeleteItem","PreDeleteItem method [Windows Shell]","PreDeleteItem method [Windows Shell]","IFileOperationProgressSink interface","_shell_IFileOperationProgressSink_PreDeleteItem","shell.IFileOperationProgressSink_PreDeleteItem","shobjidl_core/IFileOperationProgressSink::PreDeleteItem"]
old-location: shell\IFileOperationProgressSink_PreDeleteItem.htm
tech.root: shell
ms.assetid: bf54f2da-4861-4546-9b1e-35b5983e836c
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink interface [Windows Shell],PreDeleteItem method, IFileOperationProgressSink.PreDeleteItem, IFileOperationProgressSink::PreDeleteItem, PreDeleteItem, PreDeleteItem method [Windows Shell], PreDeleteItem method [Windows Shell],IFileOperationProgressSink interface, _shell_IFileOperationProgressSink_PreDeleteItem, shell.IFileOperationProgressSink_PreDeleteItem, shobjidl_core/IFileOperationProgressSink::PreDeleteItem
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
 - IFileOperationProgressSink::PreDeleteItem
 - shobjidl_core/IFileOperationProgressSink::PreDeleteItem
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
 - IFileOperationProgressSink.PreDeleteItem
---

# IFileOperationProgressSink::PreDeleteItem


## -description

Performs caller-implemented actions before the delete process for each item begins.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

bitwise value that contains flags that control the operation. See <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> for flag descriptions.

### -param psiItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that specifies the item to be deleted.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. In the case of an error value, the delete operation and all subsequent operations pending from the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> are canceled.