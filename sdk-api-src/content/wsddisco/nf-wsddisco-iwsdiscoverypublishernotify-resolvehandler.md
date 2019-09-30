---
UID: NF:wsddisco.IWSDiscoveryPublisherNotify.ResolveHandler
title: IWSDiscoveryPublisherNotify::ResolveHandler (wsddisco.h)
author: windows-sdk-content
description: Is called when a Resolve is received by the discovery publisher.
old-location: ncd\iwsdiscoverypublishernotify_resolvehandler_method.htm
tech.root: WsdApi
ms.assetid: b0dd2b82-5d08-4dd3-8e6a-892ebaf71045
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisherNotify interface,ResolveHandler method, IWSDiscoveryPublisherNotify.ResolveHandler, IWSDiscoveryPublisherNotify::ResolveHandler, ResolveHandler, ResolveHandler method, ResolveHandler method,IWSDiscoveryPublisherNotify interface, ncd.iwsdiscoverypublishernotify_resolvehandler_method, wsddisco/IWSDiscoveryPublisherNotify::ResolveHandler
ms.topic: method
f1_keywords:
- wsddisco/IWSDiscoveryPublisherNotify.ResolveHandler
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
- IWSDiscoveryPublisherNotify.ResolveHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryPublisherNotify::ResolveHandler


## -description


Is called when a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolve-message">Resolve</a> is received by the discovery publisher.


## -parameters




### -param pSoap [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_message">WSD_SOAP_MESSAGE</a> structure that contains the Resolve message received by the discovery publisher.


### -param pMessageParameters [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> interface that contains transport information associated with the received message.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



<b>ResolveHandler</b> is called whenever a Resolve is received by the discovery publisher. It is the responsibility of the callback interface to then call <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchresolve">MatchResolve</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchresolveex">MatchResolveEx</a> with host information to determine whether or not the received Resolve matches the host.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublishernotify">IWSDiscoveryPublisherNotify</a>
 

 

