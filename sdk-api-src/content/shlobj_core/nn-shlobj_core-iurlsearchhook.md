---
UID: NN:shlobj_core.IURLSearchHook
title: IURLSearchHook (shlobj_core.h)
description: Exposes a method that is used by the browser to translate the address of an unknown URL protocol.
helpviewer_keywords: ["IURLSearchHook","IURLSearchHook interface [Windows Shell]","IURLSearchHook interface [Windows Shell]","described","_win32_IURLSearchHook","shell.IURLSearchHook","shlobj_core/IURLSearchHook"]
old-location: shell\IURLSearchHook.htm
tech.root: shell
ms.assetid: 6073ad95-03b5-4c06-9742-836719211e24
ms.date: 12/05/2018
ms.keywords: IURLSearchHook, IURLSearchHook interface [Windows Shell], IURLSearchHook interface [Windows Shell],described, _win32_IURLSearchHook, shell.IURLSearchHook, shlobj_core/IURLSearchHook
f1_keywords:
- shlobj_core/IURLSearchHook
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IURLSearchHook
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IURLSearchHook interface


## -description


Exposes a method that is used by the browser to translate the address of an unknown URL protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IURLSearchHook</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IURLSearchHook</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IURLSearchHook</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iurlsearchhook-translate">Translate</a>
</td>
<td align="left" width="63%">
Called by the browser when the browser cannot determine the protocol of a URL address.

</td>
</tr>
</table> 


## -remarks



When attempting to browse to a URL address that does not contain a protocol, the browser will first attempt to determine the correct protocol from the address. If this is not successful, the browser will create URL Search Hook objects and call each object's <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iurlsearchhook-translate">Translate</a> method until the address is translated or all of the hooks have been queried.

URL Search Hooks are registered by adding a value that contains the object's class identifier (CLSID) string under the following key in the registry: 
				
				<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Internet Explorer</b>
            <b>UrlSearchHooks</b></pre>


Implement this interface if your application defines a custom URL protocol and if address translation for this protocol is required.

You do not typically use this interface; it is called by the browser.



