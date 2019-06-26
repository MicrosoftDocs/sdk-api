---
UID: NN:msaatext.IAccClientDocMgr
title: IAccClientDocMgr (msaatext.h)
author: windows-sdk-content
description: Exposes methods for client applications to retrieve documents.
old-location: winauto\iaccclientdocmgr.htm
tech.root: WinAuto
ms.assetid: 29d9c39c-0067-4ec4-b49c-13a174ff8722
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccClientDocMgr, IAccClientDocMgr interface [Windows Accessibility], IAccClientDocMgr interface [Windows Accessibility],described, msaa.iaccclientdocmgr, msaatext/IAccClientDocMgr, winauto.iaccclientdocmgr
ms.topic: interface
f1_keywords: 
 - "msaatext/IAccClientDocMgr"
req.header: msaatext.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.h
api_name:
 - IAccClientDocMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccClientDocMgr interface


## -description


<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="https://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		]

Exposes methods for client applications to retrieve documents.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccClientDocMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccClientDocMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccClientDocMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccclientdocmgr-getdocuments">GetDocuments</a>
</td>
<td align="left" width="63%">
Retrieves a list of documents that have been registered with the Microsoft Active Accessibility run time. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccclientdocmgr-getfocused">GetFocused</a>
</td>
<td align="left" width="63%">
Retrieves the document that has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccclientdocmgr-lookupbyhwnd">LookupByHWND</a>
</td>
<td align="left" width="63%">
Retrieves a document from an HWND.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccclientdocmgr-lookupbypoint">LookupByPoint</a>
</td>
<td align="left" width="63%">
Retrieves a document from a point on the screen.

</td>
</tr>
</table> 

