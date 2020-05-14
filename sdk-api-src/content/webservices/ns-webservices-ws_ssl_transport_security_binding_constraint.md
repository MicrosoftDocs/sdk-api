---
UID: NS:webservices._WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
title: WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT (webservices.h)
description: A security binding constraint that corresponds to the WS_SSL_TRANSPORT_SECURITY_BINDING.helpviewer_keywords: ["WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT","WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows]","webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT","wsw.ws_ssl_transport_security_binding_constraint"]
old-location: wsw\ws_ssl_transport_security_binding_constraint.htm
tech.root: wsw
ms.assetid: 1f547d95-0a9a-44c5-81db-b92880238b1d
ms.date: 12/05/2018
ms.keywords: WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT, WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT, wsw.ws_ssl_transport_security_binding_constraint
f1_keywords:
- webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
dev_langs:
- c++
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WebServices.h
api_name:
- WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
targetos: Windows
req.typenames: WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT
req.redist: 
ms.custom: 19H1
---

# WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT structure


## -description


A security binding constraint that corresponds to the 
                <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.
            


## -struct-fields




### -field bindingConstraint

The base binding constraint that this binding constraint derives from.
                

There are no binding-specific properties are defined for this binding constraint
                    at this time.
                


### -field out

When <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.
                


### -field out.clientCertCredentialRequired

 



