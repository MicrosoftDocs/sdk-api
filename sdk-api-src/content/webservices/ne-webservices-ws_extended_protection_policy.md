---
UID: NE:webservices.__unnamed_enum_67
title: WS_EXTENDED_PROTECTION_POLICY (webservices.h)
description: Defines if Extended Protection data should be validated.
helpviewer_keywords: ["WS_EXTENDED_PROTECTION_POLICY","WS_EXTENDED_PROTECTION_POLICY enumeration [Web Services for Windows]","WS_EXTENDED_PROTECTION_POLICY_ALWAYS","WS_EXTENDED_PROTECTION_POLICY_NEVER","WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED","webservices/WS_EXTENDED_PROTECTION_POLICY","webservices/WS_EXTENDED_PROTECTION_POLICY_ALWAYS","webservices/WS_EXTENDED_PROTECTION_POLICY_NEVER","webservices/WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED","wsw.ws_extended_protection_policy"]
old-location: wsw\ws_extended_protection_policy.htm
tech.root: wsw
ms.assetid: ee3685b1-0ffe-410e-a6fc-b31ed8d25b26
ms.date: 12/05/2018
ms.keywords: WS_EXTENDED_PROTECTION_POLICY, WS_EXTENDED_PROTECTION_POLICY enumeration [Web Services for Windows], WS_EXTENDED_PROTECTION_POLICY_ALWAYS, WS_EXTENDED_PROTECTION_POLICY_NEVER, WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED, webservices/WS_EXTENDED_PROTECTION_POLICY, webservices/WS_EXTENDED_PROTECTION_POLICY_ALWAYS, webservices/WS_EXTENDED_PROTECTION_POLICY_NEVER, webservices/WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED, wsw.ws_extended_protection_policy
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: v.1.0
req.target-min-winversvr: 
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
req.typenames: WS_EXTENDED_PROTECTION_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_EXTENDED_PROTECTION_POLICY
 - webservices/WS_EXTENDED_PROTECTION_POLICY
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
 - WS_EXTENDED_PROTECTION_POLICY
---

# WS_EXTENDED_PROTECTION_POLICY enumeration


## -description

Defines if <a href="/windows/desktop/wsw/extended-protection">Extended Protection</a> data should be validated. This property is only available on the server,
                and can only be set when <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CHANNEL_BINDING</a> with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and either <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> or <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> is used.

## -enum-fields

### -field WS_EXTENDED_PROTECTION_POLICY_NEVER:1

Extended protection data is not validated.

### -field WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED:2

If the client system supports the extended protection feature, extended protection data is looked for and validated during authentication. Otherwise it is ignored.
                

A server can detect whether the client's operating system supports extended protection but chose not to include the extended protection data or 
                    whether it does not support extended protection. The former case is insecure and thus rejected. The latter is allowed when using this flag.
                

NOTE: If the client supports the extended protection feature, but did not include extended protection data in the authentication data, this setting will cause requests to fail. This 
                    scenario is possible when the operating system was patched but the client web services implementation does not send the necessary data.
                

This is the default.

### -field WS_EXTENDED_PROTECTION_POLICY_ALWAYS:3

Extended protection data is required to be present and is always validated. Clients that are not extended-protection-aware cannot authenticate to a server 
                    setting this flag.
