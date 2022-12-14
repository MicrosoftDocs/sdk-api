---
UID: NF:shobjidl_core.IInitializeWithBindCtx.Initialize
title: IInitializeWithBindCtx::Initialize (shobjidl_core.h)
description: Initializes a handler with a bind context.
helpviewer_keywords: ["IInitializeWithBindCtx interface [Windows Shell]","Initialize method","IInitializeWithBindCtx.Initialize","IInitializeWithBindCtx::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeWithBindCtx interface","_shell_IInitializeWithBindCtx_Initialize","shell.IInitializeWithBindCtx_Initialize","shobjidl_core/IInitializeWithBindCtx::Initialize"]
old-location: shell\IInitializeWithBindCtx_Initialize.htm
tech.root: shell
ms.assetid: 5cb3117f-7e9f-463f-806c-4955cebc1c2d
ms.date: 12/05/2018
ms.keywords: IInitializeWithBindCtx interface [Windows Shell],Initialize method, IInitializeWithBindCtx.Initialize, IInitializeWithBindCtx::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithBindCtx interface, _shell_IInitializeWithBindCtx_Initialize, shell.IInitializeWithBindCtx_Initialize, shobjidl_core/IInitializeWithBindCtx::Initialize
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IInitializeWithBindCtx::Initialize
 - shobjidl_core/IInitializeWithBindCtx::Initialize
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
 - IInitializeWithBindCtx.Initialize
---

# IInitializeWithBindCtx::Initialize


## -description

Initializes a handler with a bind context.

## -parameters

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.