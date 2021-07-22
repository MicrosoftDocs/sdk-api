---
UID: NF:objidl.IBindCtx.ReleaseBoundObjects
title: IBindCtx::ReleaseBoundObjects (objidl.h)
description: Releases all pointers to all objects that were previously registered by calls to RegisterObjectBound.
helpviewer_keywords: ["IBindCtx interface [COM]","ReleaseBoundObjects method","IBindCtx.ReleaseBoundObjects","IBindCtx::ReleaseBoundObjects","ReleaseBoundObjects","ReleaseBoundObjects method [COM]","ReleaseBoundObjects method [COM]","IBindCtx interface","_com_ibindctx_releaseboundobjects","com.ibindctx_releaseboundobjects","objidl/IBindCtx::ReleaseBoundObjects"]
old-location: com\ibindctx_releaseboundobjects.htm
tech.root: com
ms.assetid: 12107633-6e7f-4d41-8e5c-5739cff98552
ms.date: 12/05/2018
ms.keywords: IBindCtx interface [COM],ReleaseBoundObjects method, IBindCtx.ReleaseBoundObjects, IBindCtx::ReleaseBoundObjects, ReleaseBoundObjects, ReleaseBoundObjects method [COM], ReleaseBoundObjects method [COM],IBindCtx interface, _com_ibindctx_releaseboundobjects, com.ibindctx_releaseboundobjects, objidl/IBindCtx::ReleaseBoundObjects
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IBindCtx::ReleaseBoundObjects
 - objidl/IBindCtx::ReleaseBoundObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IBindCtx.ReleaseBoundObjects
---

# IBindCtx::ReleaseBoundObjects


## -description

Releases all pointers to all objects that were previously registered by calls to <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">RegisterObjectBound</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You rarely call this method directly. The system's <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> implementation calls this method when the pointer to the <b>IBindCtx</b> interface on the bind context is released (the bind context is released). If a bind context is not released, all of the registered objects remain active.

If the same object has been registered more than once, this method calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method on the object the number of times it was registered.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>
