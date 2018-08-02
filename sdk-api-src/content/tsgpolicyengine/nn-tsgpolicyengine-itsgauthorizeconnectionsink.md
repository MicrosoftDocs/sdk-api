---
UID: NN:tsgpolicyengine.ITSGAuthorizeConnectionSink
title: ITSGAuthorizeConnectionSink
author: windows-sdk-content
description: Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an attempt to authorize a connection.
old-location: termserv\itsgauthorizeconnectionsink.htm
old-project: TermServ
ms.assetid: 4aa6ec0d-6525-46e1-ba0b-29d80c5ee0f1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITSGAuthorizeConnectionSink, ITSGAuthorizeConnectionSink interface [Remote Desktop Services], ITSGAuthorizeConnectionSink interface [Remote Desktop Services],described, termserv.itsgauthorizeconnectionsink, tsgpolicyengine/ITSGAuthorizeConnectionSink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PolicyAttributeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGAuthorizeConnectionSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSGAuthorizeConnectionSink interface


## -description


Exposes methods that notify Remote Desktop Gateway (RD Gateway) about the result of an  attempt to authorize a connection. The authorization plug-in should not implement this interface because it is already implemented. A pointer to this interface is passed to the authorization plug-in when RD Gateway calls the <a href="https://msdn.microsoft.com/41a61eef-c8fe-4e08-b793-a58553f31646">AuthorizeConnection</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGAuthorizeConnectionSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITSGAuthorizeConnectionSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1151aa89-944b-4497-8a8c-c6d67fbd4051">OnConnectionAuthorized</a>
</td>
<td align="left" width="63%">
Notifies RD Gateway about the result of an  attempt to authorize a connection.

</td>
</tr>
</table> 

