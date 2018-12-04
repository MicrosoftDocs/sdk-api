---
UID: NF:wsddisco.IWSDiscoveryPublisherNotify.ProbeHandler
title: IWSDiscoveryPublisherNotify::ProbeHandler
author: windows-sdk-content
description: Is called when a Probe is received by the discovery publisher.
old-location: ncd\iwsdiscoverypublishernotify_probehandler_method.htm
tech.root: wsdapi
ms.assetid: d92ce49c-308b-49e2-9646-f1eec2151441
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWSDiscoveryPublisherNotify interface,ProbeHandler method, IWSDiscoveryPublisherNotify.ProbeHandler, IWSDiscoveryPublisherNotify::ProbeHandler, ProbeHandler, ProbeHandler method, ProbeHandler method,IWSDiscoveryPublisherNotify interface, ncd.iwsdiscoverypublishernotify_probehandler_method, wsddisco/IWSDiscoveryPublisherNotify::ProbeHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWSDiscoveryPublisherNotify.ProbeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveryPublisherNotify::ProbeHandler


## -description


Is called when a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> is received by the discovery publisher.


## -parameters




### -param pSoap [in]

Pointer to a <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure that contains the Probe message received by the discovery publisher.


### -param pMessageParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> interface that contains transport information associated with the received message.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



<b>ProbeHandler</b> is called whenever a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> is received by the discovery publisher. It is the responsibility of the callback interface to then call <a href="https://msdn.microsoft.com/657f50ad-128f-4ccb-b89a-ed88f5d9b381">MatchProbe</a> or <a href="https://msdn.microsoft.com/d2441bdc-848b-48c4-bc4e-5b8f854cc4a5">MatchProbeEx</a> with host information to determine whether or not the received Probe matches the host.

The body of the Probe message passed to <i>pSoap</i> can be cast to a <a href="https://msdn.microsoft.com/f84f7e77-ffe2-41af-a10f-a626466e9847">WSD_PROBE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/6e7e0ab8-dffe-47c2-916c-a6734eb4ac44">IWSDiscoveryPublisherNotify</a>
 

 

