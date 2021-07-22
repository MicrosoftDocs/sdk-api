---
UID: NF:shobjidl_core.IThumbnailHandlerFactory.GetThumbnailHandler
title: IThumbnailHandlerFactory::GetThumbnailHandler (shobjidl_core.h)
description: Gets the requested thumbnail handler for the thumbnail of a given item.
helpviewer_keywords: ["GetThumbnailHandler","GetThumbnailHandler method [Windows Shell]","GetThumbnailHandler method [Windows Shell]","IThumbnailHandlerFactory interface","IThumbnailHandlerFactory interface [Windows Shell]","GetThumbnailHandler method","IThumbnailHandlerFactory.GetThumbnailHandler","IThumbnailHandlerFactory::GetThumbnailHandler","_shell_IThumbnailHandlerFactory_GetThumbnailHandler","shell.IThumbnailHandlerFactory_GetThumbnailHandler","shobjidl_core/IThumbnailHandlerFactory::GetThumbnailHandler"]
old-location: shell\IThumbnailHandlerFactory_GetThumbnailHandler.htm
tech.root: shell
ms.assetid: ddd0caba-079f-4b22-8c89-6ba09adeba60
ms.date: 12/05/2018
ms.keywords: GetThumbnailHandler, GetThumbnailHandler method [Windows Shell], GetThumbnailHandler method [Windows Shell],IThumbnailHandlerFactory interface, IThumbnailHandlerFactory interface [Windows Shell],GetThumbnailHandler method, IThumbnailHandlerFactory.GetThumbnailHandler, IThumbnailHandlerFactory::GetThumbnailHandler, _shell_IThumbnailHandlerFactory_GetThumbnailHandler, shell.IThumbnailHandlerFactory_GetThumbnailHandler, shobjidl_core/IThumbnailHandlerFactory::GetThumbnailHandler
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
 - IThumbnailHandlerFactory::GetThumbnailHandler
 - shobjidl_core/IThumbnailHandlerFactory::GetThumbnailHandler
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
 - IThumbnailHandlerFactory.GetThumbnailHandler
---

# IThumbnailHandlerFactory::GetThumbnailHandler


## -description

Gets the requested thumbnail handler for the thumbnail of a given item.

## -parameters

### -param pidlChild [in]

Type: <b>PCUITEMID_CHILD</b>

The item within the namespace for which the thumbnail handler is being retrieved.

### -param pbc [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> to be used during the moniker binding operation of this process.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface requested. This is usually <a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailprovider">IThumbnailProvider</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the requested thumbnail handler. If this method fails, this value is <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Windows Vista calls the <b>IThumbnailHandlerFactory::GetThumbnailHandler</b> method before falling back on <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">GetUIObjectOf</a>.