---
UID: NE:webservices.WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
title: WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
author: windows-sdk-content
description: Identifies the properties for requesting a security token from an issuer. It is used with WsRequestSecurityToken as part of the WS_REQUEST_SECURITY_TOKEN_PROPERTY* parameter.
old-location: wsw\ws_request_security_token_property_id.htm
old-project: wsw
ms.assetid: 7a2063eb-ab60-43d5-bd8c-41ef132abf50
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO, WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID enumeration [Web Services for Windows], WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE, WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE, WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS, WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES, WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION, WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION, WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS, WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS, webservices/WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION, wsw.ws_request_security_token_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_REQUEST_SECURITY_TOKEN_PROPERTY_ID enumeration


## -description



              Identifies the properties for requesting a security token from an issuer.  It is used with <a href="https://msdn.microsoft.com/ee754a7d-73a9-49ae-afc7-b443fbbe0cce">WsRequestSecurityToken</a> as part of the <a href="https://msdn.microsoft.com/ebf6d821-f540-4c89-a2f8-c795a3688e0d">WS_REQUEST_SECURITY_TOKEN_PROPERTY*</a> parameter.
            


## -enum-fields




### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_APPLIES_TO


A pointer to a <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> structure containing the address of the service ('relying party') to whom the requested
token will be presented.
                .


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_TRUST_VERSION


                    A <a href="https://msdn.microsoft.com/02a080f5-3d0d-4483-8215-bcb5b9f27b9c">WS_TRUST_VERSION</a> value that specifies the version of WS-Trust to use.


                    If this property is not specified, it defaults to <a href="https://msdn.microsoft.com/02a080f5-3d0d-4483-8215-bcb5b9f27b9c">WS_TRUST_VERSION_FEBRUARY_2005</a>.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_SECURE_CONVERSATION_VERSION

A <a href="https://msdn.microsoft.com/17c21a3a-1cb5-4174-8300-a5c3d87e3e0f">WS_SECURE_CONVERSATION_VERSION</a> value that
            specifies the version of WS-SecureConversation to use when <a href="https://msdn.microsoft.com/1ef2ab60-c0a6-461a-9c93-fce74e8d76ba">WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT</a> 
            or <b>WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT</b> are specified.
          


            If this property is not specified, it defaults to <a href="https://msdn.microsoft.com/17c21a3a-1cb5-4174-8300-a5c3d87e3e0f">WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</a>.
          


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_TYPE


                    A pointer to a <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> structure that specifies the type of the security token to be issued.  If this property is not specified,
                    the corresponding element is not generated in the request security token message, and the
                    issuer is assumed to know the token type required.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_REQUEST_ACTION


            A <a href="https://msdn.microsoft.com/1ef2ab60-c0a6-461a-9c93-fce74e8d76ba">WS_REQUEST_SECURITY_TOKEN_ACTION</a> value that specifies the action to be used with the request. The default is <b>WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE</b>.
          


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN

A pointer to a <a href="https://msdn.microsoft.com/050a2ce5-279e-48fb-85da-1d0b11cd8229">WS_SECURITY_TOKEN</a> structure that, 
            if specified, instead of requesting a new token, the provided token is renewed by requesting a new token based on 
            the existing one. The old token becomes invalid if this operation succeeds. 
            Only supported with <a href="https://msdn.microsoft.com/1ef2ab60-c0a6-461a-9c93-fce74e8d76ba">WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT</a>.
          


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_TYPE


                    A <a href="https://msdn.microsoft.com/95915a10-ba8f-41ca-89eb-777c85d2a411">WS_SECURITY_KEY_TYPE</a> value that specifies the type of the cryptographic key to be requested for the
                    issued security token.                      This must be set to <b>WS_SECURITY_KEY_TYPE_NONE</b> or <b>WS_SECURITY_KEY_TYPE_SYMMETRIC</b>.



                    The value <a href="https://msdn.microsoft.com/95915a10-ba8f-41ca-89eb-777c85d2a411">WS_SECURITY_KEY_TYPE_NONE</a> specifies a bearer token without
                    proof-of-possession keys. Such tokens will not produce a signature when used to secure a message.
                


                    If this property is not specified, the corresponding key type element is not emitted in token requests. 
                    Not emitting the key type in token requests results in the implied default of symmetric keys for the 
                    issued token, as defined in the WS-Trust specification.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_SIZE


                    A <b>ULONG</b> that specifies the size (in bits) of the cryptographic key to be requested
                    in the issued security token.  This property may be specified only for
                    issued tokens with symmetric keys.  If this property is not specified,
                    the corresponding key size element is not emitted in token requests.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_ISSUED_TOKEN_KEY_ENTROPY


                    A <a href="https://msdn.microsoft.com/dd6bca9a-e47b-46b3-b9ac-23aecb101337">WS_SECURITY_KEY_ENTROPY_MODE</a> value that specifies how entropy is contributed to the cryptographic key of the
                    issued token.  This property may be specified only for issued tokens
                    with symmetric keys.  If this property is not specified, the mode <b>WS_SECURITY_KEY_ENTROPY_MODE_SERVER_ONLY</b> is used.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS

A pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> that contains
                    the additional primary parameters to be included verbatim in request
                    security token messages.  Each such parameter must be a top-level
                    element in the supplied XML buffer.  If this property is not specified, such
                    parameters are not emitted. The buffer is serialized into the RequestSecurityToken element 
                    when requesting a security token.
                


                    Unlike <a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS</a>, local request 
                    parameters are defined by the client as a means to add parameters to the token request.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_SERVICE_REQUEST_PARAMETERS


                    A pointer to a <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> that contains
                    the service parameters to include in request security token
                    messages, supplied as an XML buffer. Each such parameter must be a
                    top-level element in the supplied XML buffer. If this is property not specified, such
                    parameters are not emitted.
                


                    If <a href="https://msdn.microsoft.com/02a080f5-3d0d-4483-8215-bcb5b9f27b9c">WS_TRUST_VERSION_FEBRUARY_2005</a> is specified this buffer is serialized
                    into the RequestSecurityToken element following the
                    <a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_LOCAL_REQUEST_PARAMETERS</a>.
                


                    If <a href="https://msdn.microsoft.com/02a080f5-3d0d-4483-8215-bcb5b9f27b9c">WS_TRUST_VERSION_1_3</a> is specified this buffer is serialized into the
                    RequestSecurityToken/SecondaryParameters element.
                 


                   Service request parameters are instructions regarding how to issue a token. They are obtained from the service, 
                   usually by means of metadata import. In that case, this parameter may be obtained 
                   from the out.RequestSecurityTokenTemplate field of the <a href="https://msdn.microsoft.com/7588f526-d1d5-486f-b317-f1a4b35e3882">WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT</a>.               
               


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_MESSAGE_PROPERTIES


                    The set of <a href="https://msdn.microsoft.com/74ad74fd-457a-4408-8032-15d365f98b14">WS_MESSAGE_PROPERTIES</a> to be specified
                    while creating the two messages with <a href="https://msdn.microsoft.com/1c48647e-9e77-4b7a-add3-e035c7f9f27e">WsCreateMessage</a> and are to
                    be used for the security token obtaining exchange.  If this property
                    is not specified, the request and reply messages are created with the
                    default message properties.
                


### -field WS_REQUEST_SECURITY_TOKEN_PROPERTY_BEARER_KEY_TYPE_VERSION



