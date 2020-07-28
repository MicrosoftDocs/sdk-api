---
UID: NN:tsgauthenticationengine.ITSGAuthenticationEngine
title: ITSGAuthenticationEngine (tsgauthenticationengine.h)
description: Exposes methods that authenticate users for Remote Desktop Gateway (RD Gateway).
helpviewer_keywords: ["ITSGAuthenticationEngine","ITSGAuthenticationEngine interface [Remote Desktop Services]","ITSGAuthenticationEngine interface [Remote Desktop Services]","described","termserv.itsgauthenticationengine","tsgauthenticationengine/ITSGAuthenticationEngine"]
old-location: termserv\itsgauthenticationengine.htm
tech.root: TermServ
ms.assetid: c72f3f22-a403-45b0-9ccb-6339ae001024
ms.date: 12/05/2018
ms.keywords: ITSGAuthenticationEngine, ITSGAuthenticationEngine interface [Remote Desktop Services], ITSGAuthenticationEngine interface [Remote Desktop Services],described, termserv.itsgauthenticationengine, tsgauthenticationengine/ITSGAuthenticationEngine
f1_keywords:
- tsgauthenticationengine/ITSGAuthenticationEngine
dev_langs:
- c++
req.header: tsgauthenticationengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGAuthenticationEngine.idl
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
- TSGAuthenticationEngine.h
api_name:
- ITSGAuthenticationEngine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAuthenticationEngine interface


## -description


Exposes methods that authenticate users for Remote Desktop Gateway (RD Gateway). Implement this interface when you want to override the default authentication process in RD Gateway.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthenticationEngine</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAuthenticationEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSGAuthenticationEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a>
</td>
<td align="left" width="63%">
Authenticates a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-cancelauthentication">CancelAuthentication</a>
</td>
<td align="left" width="63%">
Cancels an existing authentication request.

</td>
</tr>
</table> 

