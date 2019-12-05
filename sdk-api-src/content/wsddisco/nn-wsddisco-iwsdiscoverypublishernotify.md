---
UID: NN:wsddisco.IWSDiscoveryPublisherNotify
title: IWSDiscoveryPublisherNotify (wsddisco.h)
description: Is implemented by the client program to receive callback notifications from IWSDiscoveryPublisher.
old-location: ncd\iwsdiscoverypublishernotify.htm
tech.root: WsdApi
ms.assetid: 6e7e0ab8-dffe-47c2-916c-a6734eb4ac44
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisherNotify, IWSDiscoveryPublisherNotify interface, IWSDiscoveryPublisherNotify interface,described, ncd.iwsdiscoverypublishernotify, wsddisco/IWSDiscoveryPublisherNotify
ms.topic: interface
f1_keywords:
- wsddisco/IWSDiscoveryPublisherNotify
dev_langs:
- c++
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsdapi.dll
api_name:
- IWSDiscoveryPublisherNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryPublisherNotify interface


## -description


Is implemented by the client program to receive callback notifications from <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryPublisherNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveryPublisherNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDiscoveryPublisherNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublishernotify-probehandler">ProbeHandler</a>
</td>
<td align="left" width="63%">
Called when a Probe is received by the discovery publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublishernotify-resolvehandler">ResolveHandler</a>
</td>
<td align="left" width="63%">
Called when a Resolve is received by the discovery publisher.

</td>
</tr>
</table> 

