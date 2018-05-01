---
UID: NN:proofofpossessioncookieinfo.IProofOfPossessionCookieInfoManager
title: IProofOfPossessionCookieInfoManager
author: windows-driver-content
description: Supports the creation of proof of possession cookies.
old-location: wininet\iproofofpossessioncookieinfomanager.htm
old-project: WinInet
ms.assetid: b8b89e48-e47d-4089-a8b6-04d53227767a
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IProofOfPossessionCookieInfoManager, IProofOfPossessionCookieInfoManager interface [WinINet], IProofOfPossessionCookieInfoManager interface [WinINet], described, proofofpossessioncookieinfo/IProofOfPossessionCookieInfoManager, wininet.iproofofpossessioncookieinfomanager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: proofofpossessioncookieinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ProofOfPossessionCookieInfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MicrosoftAccountTokenProvider.dll
api_name:
-	IProofOfPossessionCookieInfoManager
product: Windows
targetos: Windows
req.lib: 
req.dll: MicrosoftAccountTokenProvider.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IProofOfPossessionCookieInfoManager interface


## -description


Supports the creation of proof of possession cookies.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProofOfPossessionCookieInfoManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProofOfPossessionCookieInfoManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProofOfPossessionCookieInfoManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7e22e0e-f84c-47e5-878f-b70459c921b8">GetCookieInfoForUri</a>
</td>
<td align="left" width="63%">
Gets cookie information for the supplied URI to be used for proof of possession cookies.

</td>
</tr>
</table> 

