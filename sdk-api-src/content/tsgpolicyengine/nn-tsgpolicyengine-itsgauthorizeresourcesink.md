---
UID: NN:tsgpolicyengine.ITSGAuthorizeResourceSink
title: ITSGAuthorizeResourceSink (tsgpolicyengine.h)
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a resource.helpviewer_keywords: ["ITSGAuthorizeResourceSink","ITSGAuthorizeResourceSink interface [Remote Desktop Services]","ITSGAuthorizeResourceSink interface [Remote Desktop Services]","described","termserv.itsgauthorizeresourcesink","tsgpolicyengine/ITSGAuthorizeResourceSink"]
old-location: termserv\itsgauthorizeresourcesink.htm
tech.root: TermServ
ms.assetid: 4656064a-41d9-428c-8260-24eea0ee83cc
ms.date: 12/05/2018
ms.keywords: ITSGAuthorizeResourceSink, ITSGAuthorizeResourceSink interface [Remote Desktop Services], ITSGAuthorizeResourceSink interface [Remote Desktop Services],described, termserv.itsgauthorizeresourcesink, tsgpolicyengine/ITSGAuthorizeResourceSink
f1_keywords:
- tsgpolicyengine/ITSGAuthorizeResourceSink
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- TSGPolicyEngine.h
api_name:
- ITSGAuthorizeResourceSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAuthorizeResourceSink interface


## -description


Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a resource. The authorization plug-in should not implement this interface because it is already implemented. A pointer to this interface is passed to the authorization plug-in when RD Gateway calls the <a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeresource">AuthorizeResource</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthorizeResourceSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAuthorizeResourceSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgauthorizeresourcesink-onchannelauthorized">OnChannelAuthorized</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway about the result of an  attempt to authorize a resource.

</td>
</tr>
</table> 

