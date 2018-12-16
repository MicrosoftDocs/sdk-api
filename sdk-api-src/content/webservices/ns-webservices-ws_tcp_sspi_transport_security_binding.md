---
UID: NS:webservices._WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING
title: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING
author: windows-sdk-content
description: The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the TCP transport.
old-location: wsw\ws_tcp_sspi_transport_security_binding.htm
tech.root: wsw
ms.assetid: c617f6cf-cedb-4d52-954c-fd4577260ca3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING, wsw.ws_tcp_sspi_transport_security_binding
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
 - WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING
product: Windows
targetos: Windows
req.typenames: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING
req.redist: 
---

# WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING structure


## -description


The security binding subtype for specifying the use of the Windows
Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO)
with the TCP transport.  A specific SSP package may be chosen using
the security binding property 
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE</a>;
if that property is not specified, SPNEGO is used by default.  The use
of NTLM is strongly discouraged due to its security weakness
(specifically, lack of server authentication).  If NTLM is to be
allowed, the security binding property <b>WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH</b> 
must be set to <b>FALSE</b>.
            

This security binding operates at the transport security level and is
supported only with the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_TCP_CHANNEL_BINDING</a>.  The
TCP/Windows SSPI combination uses the wire form defined by the 
NegotiateStreamprotocol and the .Net Message Framing specification.
            

On the client side, the security identity of the target server is
specified using the identity field of the <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> 
parameter supplied during <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a>.  If the identity is a 
<a href="https://msdn.microsoft.com/99a484f0-4d04-4998-90d9-c39194ecf3f8">WS_SPN_ENDPOINT_IDENTITY</a> or a <a href="https://msdn.microsoft.com/dc822551-6853-456f-a115-a96f64b0e056">WS_UPN_ENDPOINT_IDENTITY</a>, 
that string identity value is used directly with the SSP.  If the identity is a 
<a href="https://msdn.microsoft.com/09dea451-68ae-4052-8563-30f15c1335d6">WS_DNS_ENDPOINT_IDENTITY</a> and the value of its dns field is
'd1', or if no identity is specified in the <b>WS_ENDPOINT_ADDRESS</b> 
and the host component (according to Section 3.2.2 of 
RFC2396) the address URI
is 'd1', then the form 'host/d1' is used as the server SPN.
Specifying any other <a href="https://msdn.microsoft.com/59c851b4-6e1a-4144-9742-48d5c094d592">WS_ENDPOINT_IDENTITY</a> subtype in 
<b>WS_ENDPOINT_ADDRESS</b> will cause <b>WsOpenChannel</b> to fail.
            

With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH</a> (client side only)
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS</a> (server side only)
</li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL</a> (client side only)
</li>
</ul>



## -struct-fields




### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.
                


### -field clientCredential

The Windows Integrated Authentication credential to be used to
authenticate the client.  This is required on the client and must not
be specified on the server.
                

