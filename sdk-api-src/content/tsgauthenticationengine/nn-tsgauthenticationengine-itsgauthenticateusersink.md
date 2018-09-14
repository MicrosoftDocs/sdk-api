---
UID: NN:tsgauthenticationengine.ITSGAuthenticateUserSink
title: ITSGAuthenticateUserSink
author: windows-sdk-content
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about authentication events.
old-location: termserv\itsgauthenticateusersink.htm
tech.root: TermServ
ms.assetid: 6cc0dca7-1bc7-4229-9f3b-74d600776210
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITSGAuthenticateUserSink, ITSGAuthenticateUserSink interface [Remote Desktop Services], ITSGAuthenticateUserSink interface [Remote Desktop Services],described, termserv.itsgauthenticateusersink, tsgauthenticationengine/ITSGAuthenticateUserSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSGAuthenticateUserSink interface


## -description


Exposes methods that notify Remote Desktop Gateway (RD Gateway) about authentication events. The 
    authentication plug-in should not implement this interface because it is already implemented. A pointer to this 
    interface is passed to the authentication plug-in when RD Gateway calls the 
    <a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthenticateUserSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITSGAuthenticateUserSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/03385453-066d-40a9-bcbb-9623e4fdfadc">DisconnectUser</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that it should disconnect the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f3dd498-661c-4787-8db4-bcc43bd76294">OnUserAuthenticated</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that the authentication plug-in has successfully authenticated the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3d1e582-db1d-413d-8ec8-7fdb7c6e3609">OnUserAuthenticationFailed</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that the authentication plug-in failed to authenticate the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3706f72-d23c-49ac-9d81-3a38f8d399c8">ReauthenticateUser</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway that it should silently reauthenticate and reauthorize the user.

</td>
</tr>
</table> 

