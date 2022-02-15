---
UID: NN:wsdclient.IWSDServiceProxy
title: IWSDServiceProxy (wsdclient.h)
description: Represents a remote WSD service for client applications and middleware.
helpviewer_keywords: ["IWSDServiceProxy","IWSDServiceProxy interface","IWSDServiceProxy interface","described","ncd.iwsdserviceproxy","wsdclient/IWSDServiceProxy"]
old-location: ncd\iwsdserviceproxy.htm
tech.root: ncd
ms.assetid: 8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxy, IWSDServiceProxy interface, IWSDServiceProxy interface,described, ncd.iwsdserviceproxy, wsdclient/IWSDServiceProxy
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDServiceProxy
 - wsdclient/IWSDServiceProxy
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
 - IWSDServiceProxy
---

# IWSDServiceProxy interface


## -description

Represents a remote WSD service for client applications and middleware.

## -inheritance

The <b>IWSDServiceProxy</b> interface inherits from <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdmetadataexchange">IWSDMetadataExchange</a>. <b>IWSDServiceProxy</b> also has these types of members:

## -remarks

Service proxy objects may reside on multiple endpoints. An endpoint more completely represents a URL (contains additional useful data). For example, one endpoint may support HTTP on IPv4 addresses and another may support HTTPS on IPv6 addresses. Since the same service lives on both endpoints, it is important that the service have underlying endpoint proxy objects, with each endpoint proxy corresponding to a single endpoint at which the service is available. The endpoint proxy takes care of simple messaging requests to the service, for example, sending one-way or two-way messages.

<b>IWSDServiceProxy</b> objects are employed to obtain service metadata, send messages to the service through a service proxy, subscribe to events on the service, and bind to proxies that provide type-specific semantics.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdmetadataexchange">IWSDMetadataExchange</a>
