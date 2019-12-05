---
UID: NN:tsgauthenticationengine.ITSGAuthenticateUserSink
title: ITSGAuthenticateUserSink (tsgauthenticationengine.h)
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about authentication events.
old-location: termserv\itsgauthenticateusersink.htm
tech.root: TermServ
ms.assetid: 6cc0dca7-1bc7-4229-9f3b-74d600776210
ms.date: 12/05/2018
ms.keywords: ITSGAuthenticateUserSink, ITSGAuthenticateUserSink interface [Remote Desktop Services], ITSGAuthenticateUserSink interface [Remote Desktop Services],described, termserv.itsgauthenticateusersink, tsgauthenticationengine/ITSGAuthenticateUserSink
ms.topic: interface
f1_keywords:
- tsgauthenticationengine/ITSGAuthenticateUserSink
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
- ITSGAuthenticateUserSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAuthenticateUserSink interface


## -description


Exposes methods that notify Remote Desktop Gateway (RD Gateway) about authentication events. The 
    authentication plug-in should not implement this interface because it is already implemented. A pointer to this 
    interface is passed to the authentication plug-in when RD Gateway calls the 
    <a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthenticateUserSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAuthenticateUserSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSGAuthenticateUserSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticateusersink-disconnectuser">DisconnectUser</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that it should disconnect the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticateusersink-onuserauthenticated">OnUserAuthenticated</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that the authentication plug-in has successfully authenticated the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticateusersink-onuserauthenticationfailed">OnUserAuthenticationFailed</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that the authentication plug-in failed to authenticate the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticateusersink-reauthenticateuser">ReauthenticateUser</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that it should silently reauthenticate and reauthorize the user.

</td>
</tr>
</table> 

