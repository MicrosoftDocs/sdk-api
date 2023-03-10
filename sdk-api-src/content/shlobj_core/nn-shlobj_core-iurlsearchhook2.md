---
UID: NN:shlobj_core.IURLSearchHook2
title: IURLSearchHook2 (shlobj_core.h)
description: Exposes a method that is used by the browser to translate the address of an unknown URL protocol by using a search context object.
helpviewer_keywords: ["IURLSearchHook2","IURLSearchHook2 interface [Windows Shell]","IURLSearchHook2 interface [Windows Shell]","described","_shell_IURLSearchHook2","shell.IURLSearchHook2","shlobj_core/IURLSearchHook2"]
old-location: shell\IURLSearchHook2.htm
tech.root: shell
ms.assetid: 5a17e099-a8b4-454d-8f2e-0a45435902a4
ms.date: 12/05/2018
ms.keywords: IURLSearchHook2, IURLSearchHook2 interface [Windows Shell], IURLSearchHook2 interface [Windows Shell],described, _shell_IURLSearchHook2, shell.IURLSearchHook2, shlobj_core/IURLSearchHook2
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
 - IURLSearchHook2
 - shlobj_core/IURLSearchHook2
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
 - IURLSearchHook2
---

# IURLSearchHook2 interface


## -description

Exposes a method that is used by the browser to translate the address of an unknown URL protocol by using a search context object.

## -inheritance

The <b>IURLSearchHook2</b> interface inherits from <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook">IURLSearchHook</a>. <b>IURLSearchHook2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook">IURLSearchHook</a> interface, from which it inherits.

When attempting to browse to a URL address, if the browser retrieves an <b>IURLSearchHook2</b> interface, a search context is passed to the browser. If no <b>IURLSearchHook2</b> interface is available the browser uses <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook">IURLSearchHook</a> to determine the address of the unknown URL.
