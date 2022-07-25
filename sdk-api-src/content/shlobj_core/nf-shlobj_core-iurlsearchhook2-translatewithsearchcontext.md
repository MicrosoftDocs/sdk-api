---
UID: NF:shlobj_core.IURLSearchHook2.TranslateWithSearchContext
title: IURLSearchHook2::TranslateWithSearchContext (shlobj_core.h)
description: Called by the browser when the browser cannot determine the protocol of a URL address. This method uses a search context to determine the protocol.
helpviewer_keywords: ["IURLSearchHook2 interface [Windows Shell]","TranslateWithSearchContext method","IURLSearchHook2.TranslateWithSearchContext","IURLSearchHook2::TranslateWithSearchContext","TranslateWithSearchContext","TranslateWithSearchContext method [Windows Shell]","TranslateWithSearchContext method [Windows Shell]","IURLSearchHook2 interface","_shell_IURLSearchHook2_TranslateWithSearchContext","shell.IURLSearchHook2_TranslateWithSearchContext","shlobj_core/IURLSearchHook2::TranslateWithSearchContext"]
old-location: shell\IURLSearchHook2_TranslateWithSearchContext.htm
tech.root: shell
ms.assetid: 6143a642-e003-4268-b146-0d3d5cc907df
ms.date: 12/05/2018
ms.keywords: IURLSearchHook2 interface [Windows Shell],TranslateWithSearchContext method, IURLSearchHook2.TranslateWithSearchContext, IURLSearchHook2::TranslateWithSearchContext, TranslateWithSearchContext, TranslateWithSearchContext method [Windows Shell], TranslateWithSearchContext method [Windows Shell],IURLSearchHook2 interface, _shell_IURLSearchHook2_TranslateWithSearchContext, shell.IURLSearchHook2_TranslateWithSearchContext, shlobj_core/IURLSearchHook2::TranslateWithSearchContext
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IURLSearchHook2::TranslateWithSearchContext
 - shlobj_core/IURLSearchHook2::TranslateWithSearchContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IURLSearchHook2.TranslateWithSearchContext
---

# IURLSearchHook2::TranslateWithSearchContext


## -description

Called by the browser when the browser cannot determine the protocol of a URL address. This method uses a search context to determine the protocol.

## -parameters

### -param pwszSearchURL [out]

Type: <b>PWSTR</b>

The address of a wide character buffer that, on entry, contains the URL address for which the browser is trying to determine the protocol. On exit, this buffer contains the modified URL address if the method was successful.

### -param cchBufferSize

Type: <b>DWORD</b>

The size, in characters, of the buffer at <i>lpwszSearchURL</i>.

### -param pSearchContext [in, optional]

Type: <b><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext">ISearchContext</a>*</b>

A pointer to an <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext">ISearchContext</a> object. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.