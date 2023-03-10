---
UID: NN:wsddisco.IWSDiscoveryProvider
title: IWSDiscoveryProvider (wsddisco.h)
description: Used to discover services on the network advertised by WS-Discovery.
helpviewer_keywords: ["IWSDiscoveryProvider","IWSDiscoveryProvider interface","IWSDiscoveryProvider interface","described","ncd.iwsdiscoveryprovider","wsddisco/IWSDiscoveryProvider"]
old-location: ncd\iwsdiscoveryprovider.htm
tech.root: ncd
ms.assetid: e3d3acc2-914b-40bd-9e1e-a3a612821ab7
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProvider, IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,described, ncd.iwsdiscoveryprovider, wsddisco/IWSDiscoveryProvider
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
 - IWSDiscoveryProvider
 - wsddisco/IWSDiscoveryProvider
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
 - IWSDiscoveryProvider
---

# IWSDiscoveryProvider interface


## -description

This interface is used to discover services on the network advertised by WS-Discovery.

To get this interface, you can call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoveryprovider">WSDCreateDiscoveryProvider</a>.

## -inheritance

The <b>IWSDiscoveryProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveryProvider</b> also has these types of members:

## -remarks

The Discovery Provider represents the "client" view of WS-Discovery.

## -see-also

<a href="/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
