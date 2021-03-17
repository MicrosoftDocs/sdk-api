---
UID: NF:shobjidl_core.IShellItem2.Update
title: IShellItem2::Update (shobjidl_core.h)
description: Ensures that any cached information in this item is updated.
helpviewer_keywords: ["IShellItem2 interface [Windows Shell]","Update method","IShellItem2.Update","IShellItem2::Update","Update","Update method [Windows Shell]","Update method [Windows Shell]","IShellItem2 interface","_shell_IShellItem2_Update","shell.IShellItem2_Update","shobjidl_core/IShellItem2::Update"]
old-location: shell\IShellItem2_Update.htm
tech.root: shell
ms.assetid: 42000a83-2ee0-49b9-b3fc-328685e25c0b
ms.date: 12/05/2018
ms.keywords: IShellItem2 interface [Windows Shell],Update method, IShellItem2.Update, IShellItem2::Update, Update, Update method [Windows Shell], Update method [Windows Shell],IShellItem2 interface, _shell_IShellItem2_Update, shell.IShellItem2_Update, shobjidl_core/IShellItem2::Update
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
 - IShellItem2::Update
 - shobjidl_core/IShellItem2::Update
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
 - IShellItem2.Update
---

# IShellItem2::Update


## -description

Ensures that any cached information in this item is updated.

## -parameters

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on a bind context object.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including ERROR_FILE_NOT_FOUND if the item does not exist.