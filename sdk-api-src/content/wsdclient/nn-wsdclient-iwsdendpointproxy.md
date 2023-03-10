---
UID: NN:wsdclient.IWSDEndpointProxy
title: IWSDEndpointProxy (wsdclient.h)
description: Implements a device services messaging proxy.
helpviewer_keywords: ["IWSDEndpointProxy","IWSDEndpointProxy interface","IWSDEndpointProxy interface","described","ncd.iwsdendpointproxy","wsdclient/IWSDEndpointProxy"]
old-location: ncd\iwsdendpointproxy.htm
tech.root: ncd
ms.assetid: 58ca085f-8939-413c-8fd3-4d867b1cf490
ms.date: 12/05/2018
ms.keywords: IWSDEndpointProxy, IWSDEndpointProxy interface, IWSDEndpointProxy interface,described, ncd.iwsdendpointproxy, wsdclient/IWSDEndpointProxy
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
 - IWSDEndpointProxy
 - wsdclient/IWSDEndpointProxy
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
 - IWSDEndpointProxy
---

# IWSDEndpointProxy interface


## -description

Implements a device services messaging proxy.

## -inheritance

The <b>IWSDEndpointProxy</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDEndpointProxy</b> also has these types of members:

## -remarks

Service proxy objects may reside on multiple endpoints. An endpoint more completely represents a URL (contains additional useful data). One endpoint may support HTTP on IPv4 addresses and another may support HTTPS on IPv6 addresses. Since the same service lives on both endpoints, it is important that the service have underlying endpoint proxy objects, with each endpoint proxy corresponding to a single endpoint at which the service is available. The endpoint proxy takes care of simple messaging requests to the service, for example, sending one-way or two-way messages.

Endpoint proxies are generally used inside WSDAPI, but they can be retrieved from <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> or <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> objects to expose message-level functionality.
