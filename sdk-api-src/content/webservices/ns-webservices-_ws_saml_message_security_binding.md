---
UID: NS:webservices._WS_SAML_MESSAGE_SECURITY_BINDING
title: "_WS_SAML_MESSAGE_SECURITY_BINDING"
author: windows-sdk-content
description: The security binding subtype for specifying the use of a SAML assertion as a message security token.
old-location: wsw\ws_saml_message_security_binding.htm
tech.root: wsw
ms.assetid: 713afe9a-49b8-419a-b78b-d3b5a4a8d073
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_SAML_MESSAGE_SECURITY_BINDING, WS_SAML_MESSAGE_SECURITY_BINDING structure [Web Services for Windows], _WS_SAML_MESSAGE_SECURITY_BINDING, webservices/WS_SAML_MESSAGE_SECURITY_BINDING, wsw.ws_saml_message_security_binding
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - WS_SAML_MESSAGE_SECURITY_BINDING
product: Windows
targetos: Windows
req.typenames: WS_SAML_MESSAGE_SECURITY_BINDING
req.redist: 
---

# _WS_SAML_MESSAGE_SECURITY_BINDING structure


## -description


The security binding subtype for specifying the use of a SAML
assertion as a message security token.  The SAML token is expected to
be presented to a service in a WS-Security header according to the
bindingUsage specified.  This security binding may be included in a 
<a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">security description</a> only on the
server side.
           

Only one instance of this binding may be present in a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">security description</a>.
          This security binding is not supported with the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_NAMEDPIPE_CHANNEL_BINDING</a>.

For a <a href="https://msdn.microsoft.com/574496df-95dc-45f7-8c42-e646aec12e69">federated security</a> scenario that
involves getting a security token from an issuer and then presenting
it to a service, one may use <a href="https://msdn.microsoft.com/ee754a7d-73a9-49ae-afc7-b443fbbe0cce">WsRequestSecurityToken</a>together with the <a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> on
the client side, and this binding on the server side.
           

The extent of validation performed on the received SAML depends on the
authenticator specified.  If additional validation is required, the
application may get the received SAML assertion using 
<a href="https://msdn.microsoft.com/369f7690-6d70-401a-84aa-e5761dc874b5">WsGetMessageProperty</a> with the key <a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_SAML_ASSERTION</a> 
and do further processing.
            

With this security binding, no security binding properties may be specified:
            


## -struct-fields




### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.
                


### -field bindingUsage

How the security token corresponding to this security binding should be bound to a message.
                

                    Only <a href="https://msdn.microsoft.com/2f19877f-b79b-43c3-a3f5-93dd2940d499">WS_SUPPORTING_MESSAGE_SECURITY_USAGE</a> is

supported.  With this usage, this security binding provides client
authentication, but not message protection (such as signing,
encryption, replay detection).  Thus, this binding must be used
together with another security binding such as the <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> that provides a protected
channel.
                

To use this binding on HTTP without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>. This is not supported on the client or on TCP.


### -field authenticator

The authenticator for validating incoming SAML tokens.  This field is
required.
                

