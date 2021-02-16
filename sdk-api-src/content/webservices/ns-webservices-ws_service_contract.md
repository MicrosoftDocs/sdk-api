---
UID: NS:webservices._WS_SERVICE_CONTRACT
title: WS_SERVICE_CONTRACT (webservices.h)
description: Specifies a service contract on an endpoint.
helpviewer_keywords: ["WS_SERVICE_CONTRACT","WS_SERVICE_CONTRACT structure [Web Services for Windows]","webservices/WS_SERVICE_CONTRACT","wsw.ws_service_contract"]
old-location: wsw\ws_service_contract.htm
tech.root: wsw
ms.assetid: 77bd8c1e-0596-44d7-be99-356d052ee6c1
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_CONTRACT, WS_SERVICE_CONTRACT structure [Web Services for Windows], webservices/WS_SERVICE_CONTRACT, wsw.ws_service_contract
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_SERVICE_CONTRACT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_CONTRACT
 - webservices/_WS_SERVICE_CONTRACT
 - WS_SERVICE_CONTRACT
 - webservices/WS_SERVICE_CONTRACT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_CONTRACT
---

# WS_SERVICE_CONTRACT structure


## -description

Specifies a service contract on an <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_endpoint">endpoint</a>.

## -struct-fields

### -field contractDescription

The typed contract metadata. See <a href="/windows/desktop/api/webservices/ns-webservices-ws_contract_description">WS_CONTRACT_DESCRIPTION</a>. Optional, if <b>defaultMessageHandlerCallback</b> is given.

### -field defaultMessageHandlerCallback

Callback for processing unhandled messages. Optional if contractDescription is given.

### -field methodTable

The function table. Mandatory, if <b>contractDescription</b> is given.