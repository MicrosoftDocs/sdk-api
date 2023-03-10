---
UID: NN:wsddisco.IWSDiscoveryPublisher
title: IWSDiscoveryPublisher (wsddisco.h)
description: Provides methods for announcing hosts and managing incoming queries to hosts.
helpviewer_keywords: ["IWSDiscoveryPublisher","IWSDiscoveryPublisher interface","IWSDiscoveryPublisher interface","described","ncd.iwsdiscoverypublisher","wsddisco/IWSDiscoveryPublisher"]
old-location: ncd\iwsdiscoverypublisher.htm
tech.root: ncd
ms.assetid: 4fff1328-d315-4a26-b7d8-43a273133e08
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher, IWSDiscoveryPublisher interface, IWSDiscoveryPublisher interface,described, ncd.iwsdiscoverypublisher, wsddisco/IWSDiscoveryPublisher
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
 - IWSDiscoveryPublisher
 - wsddisco/IWSDiscoveryPublisher
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
 - IWSDiscoveryPublisher
---

# IWSDiscoveryPublisher interface


## -description

Provides methods for announcing hosts and managing incoming queries to hosts.

To get this interface, call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoverypublisher">WSDCreateDiscoveryPublisher</a>.

## -inheritance

The <b>IWSDiscoveryPublisher</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveryPublisher</b> also has these types of members:

## -remarks

 This interface represents the "server" or "host" side of <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery</a>.

## -see-also

<a href="/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
