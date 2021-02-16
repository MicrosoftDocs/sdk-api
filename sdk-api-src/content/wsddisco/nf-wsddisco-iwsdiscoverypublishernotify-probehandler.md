---
UID: NF:wsddisco.IWSDiscoveryPublisherNotify.ProbeHandler
title: IWSDiscoveryPublisherNotify::ProbeHandler (wsddisco.h)
description: Is called when a Probe is received by the discovery publisher.
helpviewer_keywords: ["IWSDiscoveryPublisherNotify interface","ProbeHandler method","IWSDiscoveryPublisherNotify.ProbeHandler","IWSDiscoveryPublisherNotify::ProbeHandler","ProbeHandler","ProbeHandler method","ProbeHandler method","IWSDiscoveryPublisherNotify interface","ncd.iwsdiscoverypublishernotify_probehandler_method","wsddisco/IWSDiscoveryPublisherNotify::ProbeHandler"]
old-location: ncd\iwsdiscoverypublishernotify_probehandler_method.htm
tech.root: ncd
ms.assetid: d92ce49c-308b-49e2-9646-f1eec2151441
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisherNotify interface,ProbeHandler method, IWSDiscoveryPublisherNotify.ProbeHandler, IWSDiscoveryPublisherNotify::ProbeHandler, ProbeHandler, ProbeHandler method, ProbeHandler method,IWSDiscoveryPublisherNotify interface, ncd.iwsdiscoverypublishernotify_probehandler_method, wsddisco/IWSDiscoveryPublisherNotify::ProbeHandler
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveryPublisherNotify::ProbeHandler
 - wsddisco/IWSDiscoveryPublisherNotify::ProbeHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisherNotify.ProbeHandler
---

# IWSDiscoveryPublisherNotify::ProbeHandler


## -description

Is called when a <a href="/windows/desktop/WsdApi/probe-message">Probe</a> is received by the discovery publisher.

## -parameters

### -param pSoap [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_message">WSD_SOAP_MESSAGE</a> structure that contains the Probe message received by the discovery publisher.

### -param pMessageParameters [in]

Pointer to an <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> interface that contains transport information associated with the received message.

## -returns

The return value is not meaningful. An implementer should return S_OK.

## -remarks

<b>ProbeHandler</b> is called whenever a <a href="/windows/desktop/WsdApi/probe-message">Probe</a> is received by the discovery publisher. It is the responsibility of the callback interface to then call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchprobe">MatchProbe</a> or <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchprobeex">MatchProbeEx</a> with host information to determine whether or not the received Probe matches the host.

The body of the Probe message passed to <i>pSoap</i> can be cast to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_probe">WSD_PROBE</a> structure.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublishernotify">IWSDiscoveryPublisherNotify</a>