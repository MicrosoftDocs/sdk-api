---
UID: NN:shlobj_core.IURLSearchHook2
title: IURLSearchHook2 (shlobj_core.h)
author: windows-sdk-content
description: Exposes a method that is used by the browser to translate the address of an unknown URL protocol by using a search context object.
old-location: shell\IURLSearchHook2.htm
tech.root: shell
ms.assetid: 5a17e099-a8b4-454d-8f2e-0a45435902a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IURLSearchHook2, IURLSearchHook2 interface [Windows Shell], IURLSearchHook2 interface [Windows Shell],described, _shell_IURLSearchHook2, shell.IURLSearchHook2, shlobj_core/IURLSearchHook2
ms.topic: interface
f1_keywords: 
 - "shlobj_core/IURLSearchHook2"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IURLSearchHook2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IURLSearchHook2 interface


## -description


Exposes a method that is used by the browser to translate the address of an unknown URL protocol by using a search context object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IURLSearchHook2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook">IURLSearchHook</a>. <b>IURLSearchHook2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IURLSearchHook2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iurlsearchhook2-translatewithsearchcontext">TranslateWithSearchContext</a>
</td>
<td align="left" width="63%">
Called by the browser when the browser cannot determine the protocol of a URL address. This method uses a search context to determine the protocol.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook">IURLSearchHook</a> interface, from which it inherits.

When attempting to browse to a URL address, if the browser retrieves an <b>IURLSearchHook2</b> interface, a search context is passed to the browser. If no <b>IURLSearchHook2</b> interface is available the browser uses <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook">IURLSearchHook</a> to determine the address of the unknown URL.



