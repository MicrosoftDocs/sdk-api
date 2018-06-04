---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _WS_HTTP_HEADER_AUTH_SECURITY_BINDING structure


## -description



                The security binding subtype for specifying the use of HTTP header authentication against a target service or a HTTP proxy server 
                based on the basic, digest (RFC 2617) and the SPNEGO (RFC4559) protocols.
                Since this security binding operates at the HTTP header level, it is supported only with the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>. 
                By default, this security binding is used for the target service. However  <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET</a> 
                security binding property can be specified to use it for a HTTP proxy server. This binding provides client authentication, but not message protection
                since the HTTP body is unaffected by this binding. While this security binding can be used alone, such usage is not recommended;
                more typically, HTTP header authentication is done in conjunction with transport level security provided by a security binding such as the 
                <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>. To use this binding without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>.


With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET</a> (client side only)</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_BASIC_REALM</a> (server side only)</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_REALM</a> (server side only)</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_DOMAIN</a> (server side only)</li>
</ul>



## -struct-fields




### -field binding


The base type from which this security binding subtype and all other security binding subtypes derive.
                


### -field clientCredential


The Windows Integrated Authentication credential to be used to
authenticate the client.  This is required on the client side and must
be <b>NULL</b> on the server side.
                


                    If the credential used is a <a href="https://msdn.microsoft.com/14753a2d-6054-4041-a72b-4cd7a9576f3b">WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> then 
                    <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME</a> must be set to 
                    <a href="https://msdn.microsoft.com/c96e10ee-29d1-4c66-9f4d-64e663b25fd0">WS_HTTP_HEADER_AUTH_SCHEME_NONE</a>, <b>WS_HTTP_HEADER_AUTH_SCHEME_NTLM</b>, 
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</b> or <b>WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT</b>.
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT</b> defaults to using the Passport keyring.
                

