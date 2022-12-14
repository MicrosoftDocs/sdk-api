---
UID: NF:shobjidl_core.ITransferSource.LinkItem
title: ITransferSource::LinkItem (shobjidl_core.h)
description: Not implemented. (ITransferSource.LinkItem)
helpviewer_keywords: ["ITransferSource interface [Windows Shell]","LinkItem method","ITransferSource.LinkItem","ITransferSource::LinkItem","LinkItem","LinkItem method [Windows Shell]","LinkItem method [Windows Shell]","ITransferSource interface","_shell_ITransferSource_LinkItem","shell.ITransferSource_LinkItem","shobjidl_core/ITransferSource::LinkItem"]
old-location: shell\ITransferSource_LinkItem.htm
tech.root: shell
ms.assetid: e373c790-5366-4bff-a08d-817b0c566b1d
ms.date: 12/05/2018
ms.keywords: ITransferSource interface [Windows Shell],LinkItem method, ITransferSource.LinkItem, ITransferSource::LinkItem, LinkItem, LinkItem method [Windows Shell], LinkItem method [Windows Shell],ITransferSource interface, _shell_ITransferSource_LinkItem, shell.ITransferSource_LinkItem, shobjidl_core/ITransferSource::LinkItem
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
 - ITransferSource::LinkItem
 - shobjidl_core/ITransferSource::LinkItem
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
 - ITransferSource.LinkItem
---

# ITransferSource::LinkItem


## -description

Not implemented.

## -parameters

### -param psiSource [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the source item.

### -param psiParentDest [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> as parent to link.

### -param pszNewName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string containing the name for the link.

### -param flags [in]

Type: <b>DWORD</b>

The flags that control the file operation. Value is one or more of the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags">TRANSFER_SOURCE_FLAGS</a> constants.

### -param ppsiNewDest [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>**</b>

When the method returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> of the link.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
