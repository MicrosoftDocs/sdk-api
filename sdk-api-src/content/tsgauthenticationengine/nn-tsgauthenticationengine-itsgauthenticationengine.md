---
UID: NN:tsgauthenticationengine.ITSGAuthenticationEngine
title: ITSGAuthenticationEngine
author: windows-sdk-content
description: Exposes methods that authenticate users for Remote Desktop Gateway (RD Gateway).
old-location: termserv\itsgauthenticationengine.htm
old-project: TermServ
ms.assetid: c72f3f22-a403-45b0-9ccb-6339ae001024
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ITSGAuthenticationEngine, ITSGAuthenticationEngine interface [Remote Desktop Services], ITSGAuthenticationEngine interface [Remote Desktop Services],described, termserv.itsgauthenticationengine, tsgauthenticationengine/ITSGAuthenticationEngine
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
tech.root: 
req.typenames: TRANSPORT_SETTING_ID, *PTRANSPORT_SETTING_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TSGAuthenticationEngine.h
api_name:
-	ITSGAuthenticationEngine
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSGAuthenticationEngine interface


## -description


Exposes methods that authenticate users for Remote Desktop Gateway (RD Gateway). Implement this interface when you want to override the default authentication process in RD Gateway.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthenticationEngine</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITSGAuthenticationEngine</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a>
</td>
<td align="left" width="63%">
Authenticates a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07da9ffa-b137-4e99-a1d1-14b7c14438a3">CancelAuthentication</a>
</td>
<td align="left" width="63%">
Cancels an existing authentication request.

</td>
</tr>
</table> 

