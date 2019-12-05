---
UID: NN:tsgpolicyengine.ITSGAuthorizeConnectionSink
title: ITSGAuthorizeConnectionSink (tsgpolicyengine.h)
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a connection.
old-location: termserv\itsgauthorizeconnectionsink.htm
tech.root: TermServ
ms.assetid: 4aa6ec0d-6525-46e1-ba0b-29d80c5ee0f1
ms.date: 12/05/2018
ms.keywords: ITSGAuthorizeConnectionSink, ITSGAuthorizeConnectionSink interface [Remote Desktop Services], ITSGAuthorizeConnectionSink interface [Remote Desktop Services],described, termserv.itsgauthorizeconnectionsink, tsgpolicyengine/ITSGAuthorizeConnectionSink
ms.topic: interface
f1_keywords:
- tsgpolicyengine/ITSGAuthorizeConnectionSink
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
- ITSGAuthorizeConnectionSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAuthorizeConnectionSink interface


## -description


Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a connection. The authorization plug-in should not implement this interface because it is already implemented. A pointer to this interface is passed to the authorization plug-in when RD Gateway calls the <a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgpolicyengine-authorizeconnection">AuthorizeConnection</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthorizeConnectionSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSGAuthorizeConnectionSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSGAuthorizeConnectionSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsgpolicyengine/nf-tsgpolicyengine-itsgauthorizeconnectionsink-onconnectionauthorized">OnConnectionAuthorized</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway about the result of an  attempt to authorize a connection.

</td>
</tr>
</table> 

