---
UID: NS:webservices._WS_USERNAME_MESSAGE_SECURITY_BINDING
title: WS_USERNAME_MESSAGE_SECURITY_BINDING (webservices.h)
description: The security binding subtype for specifying the use of an application supplied username / password pair as a direct (i.e., one-shot) security token.
helpviewer_keywords: ["WS_USERNAME_MESSAGE_SECURITY_BINDING","WS_USERNAME_MESSAGE_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING","wsw.ws_username_message_security_binding"]
old-location: wsw\ws_username_message_security_binding.htm
tech.root: wsw
ms.assetid: be6d4787-fa50-4260-8236-39dd992adcae
ms.date: 12/05/2018
ms.keywords: WS_USERNAME_MESSAGE_SECURITY_BINDING, WS_USERNAME_MESSAGE_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING, wsw.ws_username_message_security_binding
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
req.typenames: WS_USERNAME_MESSAGE_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_USERNAME_MESSAGE_SECURITY_BINDING
 - webservices/_WS_USERNAME_MESSAGE_SECURITY_BINDING
 - WS_USERNAME_MESSAGE_SECURITY_BINDING
 - webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING
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
 - WS_USERNAME_MESSAGE_SECURITY_BINDING
---

# WS_USERNAME_MESSAGE_SECURITY_BINDING structure


## -description

The security binding subtype for specifying the use of an application
supplied username / password pair as a direct (i.e., one-shot)
security token.  This security binding may be used only with message
security.  It provides client authentication, but not traffic signing
or encryption.  So, it is used in conjunction with another transport
security or message security binding that provides message protection.
            

Only one instance of this binding may be present in a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">security description</a>.
          This security binding is not supported with the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_NAMEDPIPE_CHANNEL_BINDING</a>.

With this security binding, no security binding properties may be specified.

## -struct-fields

### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.

### -field bindingUsage

How the security token corresponding to this security binding should be bound to a message.
                

Only <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_security_usage">WS_SUPPORTING_MESSAGE_SECURITY_USAGE</a> is
supported.  With this usage, this security binding provides client
authentication, but not message protection (such as signing, encryption,
replay detection).  Thus, this binding must be used together with
                        another security binding such as the <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> 
                        that provides a protected channel.


To use this binding on HTTP without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>. This is not supported on the client or on TCP.

### -field clientCredential

The username credential to be used with this security binding.  This
must be specified when this security binding is used on the
client.

### -field passwordValidator

The validator to be used to check received username/password pairs.
This must be specified when this security binding is used on the
service.

### -field passwordValidatorCallbackState

The optional state to be passed in as an argument when the username validator is invoked.