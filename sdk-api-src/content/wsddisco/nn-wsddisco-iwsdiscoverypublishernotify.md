---
UID: NN:wsddisco.IWSDiscoveryPublisherNotify
title: IWSDiscoveryPublisherNotify
author: windows-sdk-content
description: Is implemented by the client program to receive callback notifications from IWSDiscoveryPublisher.
old-location: ncd\iwsdiscoverypublishernotify.htm
old-project: wsdapi
ms.assetid: 6e7e0ab8-dffe-47c2-916c-a6734eb4ac44
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: IWSDiscoveryPublisherNotify, IWSDiscoveryPublisherNotify interface, IWSDiscoveryPublisherNotify interface,described, ncd.iwsdiscoverypublishernotify, wsddisco/IWSDiscoveryPublisherNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisherNotify
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryPublisherNotify interface


## -description


Is implemented by the client program to receive callback notifications from <a href="https://msdn.microsoft.com/4fff1328-d315-4a26-b7d8-43a273133e08">IWSDiscoveryPublisher</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryPublisherNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDiscoveryPublisherNotify</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d92ce49c-308b-49e2-9646-f1eec2151441">ProbeHandler</a>
</td>
<td align="left" width="63%">
Called when a Probe is received by the discovery publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0dd2b82-5d08-4dd3-8e6a-892ebaf71045">ResolveHandler</a>
</td>
<td align="left" width="63%">
Called when a Resolve is received by the discovery publisher.

</td>
</tr>
</table> 

