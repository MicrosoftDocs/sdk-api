---
UID: NF:shobjidl_core.IInitializeWithItem.Initialize
title: IInitializeWithItem::Initialize (shobjidl_core.h)
description: Initializes a handler with an IShellItem.
helpviewer_keywords: ["IInitializeWithItem interface [Windows Shell]","Initialize method","IInitializeWithItem.Initialize","IInitializeWithItem::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeWithItem interface","STGM_READ","STGM_READWRITE","shell.IInitializeWithItem_Initialize","shell_IInitializeWithItem_Initialize","shobjidl_core/IInitializeWithItem::Initialize"]
old-location: shell\IInitializeWithItem_Initialize.htm
tech.root: shell
ms.assetid: 61abf5c8-2847-4788-9d99-65f3b1c821d6
ms.date: 12/05/2018
ms.keywords: IInitializeWithItem interface [Windows Shell],Initialize method, IInitializeWithItem.Initialize, IInitializeWithItem::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithItem interface, STGM_READ, STGM_READWRITE, shell.IInitializeWithItem_Initialize, shell_IInitializeWithItem_Initialize, shobjidl_core/IInitializeWithItem::Initialize
req.header: shobjidl_core.h
req.include-header: Propsys.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IInitializeWithItem::Initialize
 - shobjidl_core/IInitializeWithItem::Initialize
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
 - IInitializeWithItem.Initialize
---

# IInitializeWithItem::Initialize


## -description

Initializes a handler with an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param grfMode [in]

Type: <b>DWORD</b>

One of the following <a href="/windows/desktop/Stg/stgm-constants">STGM</a> values that indicate the access mode for <i>psi</i>.



#### STGM_READ

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is read-only.



#### STGM_READWRITE

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> is read/write accessible.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> cannot be accessed, this method returns an appropriate error code.

A handler instance should be initialized only once in its lifetime. Attempts by the calling application to reinitialize the handler result in the error <code>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</code>.