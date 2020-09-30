---
UID: NN:msaatext.IAccServerDocMgr
title: IAccServerDocMgr (msaatext.h)
description: Exposes methods that make documents accessible to client applications.
helpviewer_keywords: ["IAccServerDocMgr","IAccServerDocMgr interface [Windows Accessibility]","IAccServerDocMgr interface [Windows Accessibility]","described","msaa.iaccserverdocmgr","msaatext/IAccServerDocMgr","winauto.iaccserverdocmgr"]
old-location: winauto\iaccserverdocmgr.htm
tech.root: WinAuto
ms.assetid: a69d46b1-26d2-4121-b89a-42c53343d426
ms.date: 12/05/2018
ms.keywords: IAccServerDocMgr, IAccServerDocMgr interface [Windows Accessibility], IAccServerDocMgr interface [Windows Accessibility],described, msaa.iaccserverdocmgr, msaatext/IAccServerDocMgr, winauto.iaccserverdocmgr
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccServerDocMgr
 - msaatext/IAccServerDocMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.h
api_name:
 - IAccServerDocMgr
---

# IAccServerDocMgr interface


## -description

<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		]

Exposes methods that make documents accessible to client applications.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccServerDocMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccServerDocMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccServerDocMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msaatext/nf-msaatext-iaccserverdocmgr-newdocument">NewDocument</a>
</td>
<td align="left" width="63%">
Creates a wrapped document and registers it with the store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msaatext/nf-msaatext-iaccserverdocmgr-ondocumentfocus">OnDocumentFocus</a>
</td>
<td align="left" width="63%">
Notifies the Microsoft Active Accessibility run time when a document gets or loses focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/msaatext/nf-msaatext-iaccserverdocmgr-revokedocument">RevokeDocument</a>
</td>
<td align="left" width="63%">
Notifies the Microsoft Active Accessibility run time that a document is no longer available.

</td>
</tr>
</table>