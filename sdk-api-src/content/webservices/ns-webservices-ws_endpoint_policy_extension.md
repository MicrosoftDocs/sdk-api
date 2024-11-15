---
UID: NS:webservices._WS_ENDPOINT_POLICY_EXTENSION
title: WS_ENDPOINT_POLICY_EXTENSION (webservices.h)
description: This structure is used to specify an endpoint policy extension.
helpviewer_keywords: ["WS_ENDPOINT_POLICY_EXTENSION","WS_ENDPOINT_POLICY_EXTENSION structure [Web Services for Windows]","webservices/WS_ENDPOINT_POLICY_EXTENSION","wsw.ws_endpoint_policy_extension"]
old-location: wsw\ws_endpoint_policy_extension.htm
tech.root: wsw
ms.assetid: 8bcb2466-fb07-4a15-82a2-87fc7f0f3d92
ms.date: 12/05/2018
ms.keywords: WS_ENDPOINT_POLICY_EXTENSION, WS_ENDPOINT_POLICY_EXTENSION structure [Web Services for Windows], webservices/WS_ENDPOINT_POLICY_EXTENSION, wsw.ws_endpoint_policy_extension
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
targetos: Windows
req.typenames: WS_ENDPOINT_POLICY_EXTENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ENDPOINT_POLICY_EXTENSION
 - webservices/_WS_ENDPOINT_POLICY_EXTENSION
 - WS_ENDPOINT_POLICY_EXTENSION
 - webservices/WS_ENDPOINT_POLICY_EXTENSION
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
 - WS_ENDPOINT_POLICY_EXTENSION
---

# WS_ENDPOINT_POLICY_EXTENSION structure


## -description

This structure is used to specify an endpoint policy extension.

## -struct-fields

### -field policyExtension

The base policy extension that this policy extension derives from.

### -field assertionName

Name of the assertion to be retrieved as an extension.

### -field assertionNs

Namespace of the assertion to be retrieved as an extension.

### -field out

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    fields of this structure will be filled out as follows:

### -field out.assertionValue

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR and if the specified assertion is found in the policy alternative, <b>assertionValue</b> returns the read-only content. Returned buffer should not be modified or freed. If not found, it is set to NULL.

## -remarks

This extension can be used to specify a custom assertion or an assertion that is
              supported by this library so that the application can
              retrieve the original XML form of the assertion. If one of the supported assertions
              is specified as an extension, the corresponding constraint should not be specified.
              For example, if http://schemas.xmlsoap.org/ws/2005/07/securitypolicy:TransportBinding
              is specified as an endpoint extension, <a href="/windows/win32/api/webservices/ns-webservices-ws_ssl_transport_security_binding_constraint">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> cannot be specified as a constraint.
          

The following assertions are not allowed as policy extension because they might affect constraint 
              matching result if the assertion is handled as assertion. 


``` syntax
<wsa09p:UsingAddressing.../>
<wsa10p:UsingAddressing.../>
<binp:BinaryEncoding.../>
<mtomp:OptimizedMimeSerialization.../>
```

