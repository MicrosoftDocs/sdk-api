---
UID: NE:webservices.__unnamed_enum_79
title: WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID (webservices.h)
description: Identifies the properties for requesting a security token from an issuer. It is used with WsRequestSecurityToken as part of the WS_REQUEST_SECURITY_TOKEN_PROPERTY* parameter.
helpviewer_keywords: ["WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO","WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN","WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID","WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows]","WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY","WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE","WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE","WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE","WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS","WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES","WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION","WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION","WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS","WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS","webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION","wsw.ws_request_security_token_property_id"]
old-location: wsw\ws_request_security_token_property_id.htm
tech.root: wsw
ms.assetid: 7a2063eb-ab60-43d5-bd8c-41ef132abf50
ms.date: 12/05/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO, WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows], WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE, WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS, WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES, WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION, WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION, WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS, WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION, wsw.ws_request_security_token_property_id
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
req.typenames: WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
 - webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
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
 - WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
---

# WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID enumeration


## -description

Identifies the properties for requesting a security token from an issuer.  It is used with <a href="/windows/desktop/api/webservices/nf-webservices-wsrequestsecuritytoken">WsRequestSecurityToken</a> as part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_request_security_token_property">WS_REQUEST_SECURITY_TOKEN_PROPERTY*</a> parameter.

## -enum-fields

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO:1

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> structure containing the address of the service ('relying party') to whom the requested
token will be presented.
                .

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION:2

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_trust_version">WS_TRUST_VERSION</a> value that specifies the version of WS-Trust to use.

If this property is not specified, it defaults to <a href="/windows/desktop/api/webservices/ne-webservices-ws_trust_version">WS_TRUST_VERSION_FEBRUARY_2005</a>.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION:3

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_secure_conversation_version">WS_SECURE_CONVERSATION_VERSION</a> value that
            specifies the version of WS-SecureConversation to use when <a href="/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_action">WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT</a> 
            or <b>WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT</b> are specified.
          

If this property is not specified, it defaults to <a href="/windows/desktop/api/webservices/ne-webservices-ws_secure_conversation_version">WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</a>.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE:4

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> structure that specifies the type of the security token to be issued.  If this property is not specified,
                    the corresponding element is not generated in the request security token message, and the
                    issuer is assumed to know the token type required.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION:5

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_action">WS_REQUEST_SECURITY_TOKEN_ACTION</a> value that specifies the action to be used with the request. The default is <b>WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE</b>.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN:6

A pointer to a <a href="/windows/desktop/wsw/ws-security-token">WS_SECURITY_TOKEN</a> structure that, 
            if specified, instead of requesting a new token, the provided token is renewed by requesting a new token based on 
            the existing one. The old token becomes invalid if this operation succeeds. 
            Only supported with <a href="/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_action">WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT</a>.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE:7

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_key_type">WS_SECURITY_KEY_TYPE</a> value that specifies the type of the cryptographic key to be requested for the
                    issued security token.                      This must be set to <b>WS_SECURITY_KEY_TYPE_NONE</b> or <b>WS_SECURITY_KEY_TYPE_SYMMETRIC</b>.


The value <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_key_type">WS_SECURITY_KEY_TYPE_NONE</a> specifies a bearer token without
                    proof-of-possession keys. Such tokens will not produce a signature when used to secure a message.
                

If this property is not specified, the corresponding key type element is not emitted in token requests. 
                    Not emitting the key type in token requests results in the implied default of symmetric keys for the 
                    issued token, as defined in the WS-Trust specification.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE:8

A <b>ULONG</b> that specifies the size (in bits) of the cryptographic key to be requested
                    in the issued security token.  This property may be specified only for
                    issued tokens with symmetric keys.  If this property is not specified,
                    the corresponding key size element is not emitted in token requests.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY:9

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_key_entropy_mode">WS_SECURITY_KEY_ENTROPY_MODE</a> value that specifies how entropy is contributed to the cryptographic key of the
                    issued token.  This property may be specified only for issued tokens
                    with symmetric keys.  If this property is not specified, the mode <b>WS_SECURITY_KEY_ENTROPY_MODE_SERVER_ONLY</b> is used.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS:10

A pointer to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> that contains
                    the additional primary parameters to be included verbatim in request
                    security token messages.  Each such parameter must be a top-level
                    element in the supplied XML buffer.  If this property is not specified, such
                    parameters are not emitted. The buffer is serialized into the RequestSecurityToken element 
                    when requesting a security token.
                

Unlike <a href="/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_property_id">WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS</a>, local request 
                    parameters are defined by the client as a means to add parameters to the token request.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS:11

A pointer to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> that contains
                    the service parameters to include in request security token
                    messages, supplied as an XML buffer. Each such parameter must be a
                    top-level element in the supplied XML buffer. If this is property not specified, such
                    parameters are not emitted.
                

If <a href="/windows/desktop/api/webservices/ne-webservices-ws_trust_version">WS_TRUST_VERSION_FEBRUARY_2005</a> is specified this buffer is serialized
                    into the RequestSecurityToken element following the
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_request_security_token_property_id">WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS</a>.
                

If <a href="/windows/desktop/api/webservices/ne-webservices-ws_trust_version">WS_TRUST_VERSION_1_3</a> is specified this buffer is serialized into the
                    RequestSecurityToken/SecondaryParameters element.
                 

Service request parameters are instructions regarding how to issue a token. They are obtained from the service, 
                   usually by means of metadata import. In that case, this parameter may be obtained 
                   from the out.RequestSecurityTokenTemplate field of the <a href="/windows/win32/api/webservices/ns-webservices-ws_issued_token_message_security_binding_constraint">WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES:12

The set of <a href="/windows/desktop/api/webservices/ns-webservices-ws_message_properties">WS_MESSAGE_PROPERTIES</a> to be specified
                    while creating the two messages with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatemessage">WsCreateMessage</a> and are to
                    be used for the security token obtaining exchange.  If this property
                    is not specified, the request and reply messages are created with the
                    default message properties.

### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_BEARER_KEY_TYPE_VERSION:13
