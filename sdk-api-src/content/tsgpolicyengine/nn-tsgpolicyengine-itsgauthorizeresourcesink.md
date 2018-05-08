---
UID: NN:tsgpolicyengine.ITSGAuthorizeResourceSink
title: ITSGAuthorizeResourceSink
author: windows-driver-content
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a resource.
old-location: termserv\itsgauthorizeresourcesink.htm
old-project: TermServ
ms.assetid: 4656064a-41d9-428c-8260-24eea0ee83cc
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ITSGAuthorizeResourceSink, ITSGAuthorizeResourceSink interface [Remote Desktop Services], ITSGAuthorizeResourceSink interface [Remote Desktop Services],described, termserv.itsgauthorizeresourcesink, tsgpolicyengine/ITSGAuthorizeResourceSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PolicyAttributeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TSGPolicyEngine.h
api_name:
-	ITSGAuthorizeResourceSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSGAuthorizeResourceSink interface


## -description


Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a resource. The authorization plug-in should not implement this interface because it is already implemented. A pointer to this interface is passed to the authorization plug-in when RD Gateway calls the <a href="https://msdn.microsoft.com/77950541-c94a-4035-a2d8-a6014eb387e5">AuthorizeResource</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthorizeResourceSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITSGAuthorizeResourceSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSGAuthorizeResourceSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e09247af-54ea-4846-97d5-d503a811ab29">OnChannelAuthorized</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway about the result of an  attempt to authorize a resource.

</td>
</tr>
</table> 

