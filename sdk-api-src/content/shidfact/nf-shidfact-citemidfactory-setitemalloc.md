---
UID: NF:shidfact.CItemIDFactory.SetItemAlloc
title: CItemIDFactory::SetItemAlloc (shidfact.h)
description: Provides the CItemIDFactory an IMalloc interface used to allocate and free item IDs.
helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","SetItemAlloc method","CItemIDFactory.SetItemAlloc","CItemIDFactory::SetItemAlloc","SetItemAlloc","SetItemAlloc method [Windows Shell]","SetItemAlloc method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_setitemalloc","shidfact/CItemIDFactory::SetItemAlloc"]
old-location: shell\citemidfactory_setitemalloc.htm
tech.root: shell
ms.assetid: 3E2BAAD9-5C16-4ECF-BADB-16B355439BA5
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],SetItemAlloc method, CItemIDFactory.SetItemAlloc, CItemIDFactory::SetItemAlloc, SetItemAlloc, SetItemAlloc method [Windows Shell], SetItemAlloc method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_setitemalloc, shidfact/CItemIDFactory::SetItemAlloc
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - CItemIDFactory::SetItemAlloc
 - shidfact/CItemIDFactory::SetItemAlloc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shidfact.h
api_name:
 - CItemIDFactory.SetItemAlloc
---

# CItemIDFactory::SetItemAlloc


## -description

Provides the <a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a> an <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface used to allocate and free item IDs.

## -parameters

### -param pmalloc [in, out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> interface.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder">IDelegateFolder</a>