---
UID: NS:webservices._WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
title: WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING (webservices.h)
author: windows-sdk-content
description: The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the named pipe transport.
old-location: wsw\ws_namedpipe_sspi_transport_security_binding.htm
tech.root: wsw
ms.assetid: 02FCD206-23BC-4ED0-9E4A-76AB0926FD7C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING, WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING, wsw.ws_namedpipe_sspi_transport_security_binding
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
product: Windows
targetos: Windows
req.typenames: WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
req.redist: 
---

# WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING structure


## -description


The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the named pipe transport. A specific SSP package may be chosen using the security binding property <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE</a>; if that property is not specified, SPNEGO is used by default.

This security binding operates at the transport security level and is supported only with the <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_NAMEDPIPE_CHANNEL_BINDING</a>. The NamedPipe/Windows SSPI combination uses the wire form defined by the <a href="http://msdn.microsoft.com/en-us/library/cc219293.aspx">NegotiateStream</a> protocol and the <a href="http://msdn.microsoft.com/en-us/library/cc236723.aspx">.Net Message Framing</a> specification. 

On the client side, the security identity of the target server is specified using the identity field of the <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> parameter supplied during <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a>. 



The named pipe binding supports only this one transport security binding and does not support any message security bindings. 

With this security binding, the following security binding properties may be specified: 
<ul>
<li>
<a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH</a> (client side only)</li>
<li>
<a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS</a> (server side only)</li>
<li>
<a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL</a> (client side only)</li>
</ul>This type derives from the base type <a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">WS_SECURITY_BINDING</a>. For an instance of this type, the type selector field <b>bindingType</b> must have the value <a href="https://msdn.microsoft.com/caa3d71c-420c-4be0-a371-0f2d48ebd757">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE</a>. 


## -struct-fields




### -field binding

The <a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">base type</a> from which this security binding subtype and all other security binding subtypes derive.


### -field clientCredential

The <a href="https://msdn.microsoft.com/en-us/library/Dd323506(v=VS.85).aspx">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> structure to be used to authenticate the client. This is required on the client and must not be specified on the server. 

