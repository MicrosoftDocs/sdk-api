---
UID: NS:webservices._WS_SECURITY_PROPERTY_CONSTRAINT
title: WS_SECURITY_PROPERTY_CONSTRAINT (webservices.h)
description: This structure is used to specify a set of constraints for a particular security property. Any property constraints that are not specified will use the default constraints.
helpviewer_keywords: ["WS_SECURITY_PROPERTY_CONSTRAINT","WS_SECURITY_PROPERTY_CONSTRAINT structure [Web Services for Windows]","webservices/WS_SECURITY_PROPERTY_CONSTRAINT","wsw.ws_security_property_constraint"]
old-location: wsw\ws_security_property_constraint.htm
tech.root: wsw
ms.assetid: 382d75be-2c56-44f5-8069-740ad9b9d1c4
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_PROPERTY_CONSTRAINT, WS_SECURITY_PROPERTY_CONSTRAINT structure [Web Services for Windows], webservices/WS_SECURITY_PROPERTY_CONSTRAINT, wsw.ws_security_property_constraint
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
req.typenames: WS_SECURITY_PROPERTY_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_PROPERTY_CONSTRAINT
 - webservices/_WS_SECURITY_PROPERTY_CONSTRAINT
 - WS_SECURITY_PROPERTY_CONSTRAINT
 - webservices/WS_SECURITY_PROPERTY_CONSTRAINT
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
 - WS_SECURITY_PROPERTY_CONSTRAINT
---

# WS_SECURITY_PROPERTY_CONSTRAINT structure


## -description

This structure is used to specify a set of constraints
                for a particular security property.
                Any property constraints that are not specified will use
                the default constraints.

## -struct-fields

### -field id

The id of the security property.  The following security
                    property constraints may be specified:
                

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_PROPERTY_TIMESTAMP_USAGE</a>
This property constraint may be specified when any 
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_username_message_security_binding_constraint">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_cert_message_security_binding_constraint">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_security_context_message_security_binding_constraint">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>
If this property is not specified, then the default constraint value
                        of <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_timestamp_usage">WS_SECURITY_TIMESTAMP_USAGE_ALWAYS</a> will be used.
                    

</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</a>
This property constraint may be specified when any
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_ssl_transport_security_binding_constraint">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_http_header_auth_security_binding_constraint">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>
If this property is not specified, then the default constraint value
                        of <a href="/windows/desktop/api/webservices/ne-webservices-ws_protection_level">WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT</a> will be used.
                    
<b>WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT</b> This property constraint may be specified when any
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_username_message_security_binding_constraint">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_cert_message_security_binding_constraint">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_security_context_message_security_binding_constraint">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>
If this property is not specified, then the default constraint value
                        of <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_header_layout">WS_SECURITY_HEADER_LAYOUT_STRICT</a> will be used.
                    
<b>WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION</b>This property constraint may be specified when any
                        of the following security bindings are specified:
                    

<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_username_message_security_binding_constraint">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_cert_message_security_binding_constraint">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_security_context_message_security_binding_constraint">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>
If this property is not specified, then the default constraint value
                        of <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_header_version">WS_SECURITY_HEADER_VERSION_1_1</a> will be used.
                    
<b>WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME</b>This property constraint may be specified when any
                    of the following security bindings are specified:
                  

<ul>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_username_message_security_binding_constraint">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_cert_message_security_binding_constraint">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
<li>
<a href="/windows/win32/api/webservices/ns-webservices-ws_security_context_message_security_binding_constraint">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>
</li>
</ul>
If this property is not specified, then the default constraint value
                    of <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_algorithm_suite_name">WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256</a> will be used.
                  

</li>
</ul>

### -field allowedValues

An array of values which are acceptable.  The type of
                    the values in the array correspond to the type of the values
                    of the security property.  See the documentation for
                    a particular security property to determine the type of the
                    property.

### -field allowedValuesSize

The total size of the allowedValues array, in bytes.  This
                    size must be a multiple of the size of the type of the value
                    of the property.

### -field out

When <a href="/windows/desktop/api/webservices/nf-webservices-wsmatchpolicyalternative">WsMatchPolicyAlternative</a> returns NOERROR, the
                    entire contents of this structure will be filled out.

### -field out.securityProperty