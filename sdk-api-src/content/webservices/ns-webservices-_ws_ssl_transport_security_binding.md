---
UID: NS:webservices._WS_SSL_TRANSPORT_SECURITY_BINDING
title: "_WS_SSL_TRANSPORT_SECURITY_BINDING"
author: windows-sdk-content
description: The security binding subtype for specifying the use of SSL/TLS protocol based transport security.
old-location: wsw\ws_ssl_transport_security_binding.htm
old-project: wsw
ms.assetid: 078efc1d-a1bc-4035-919c-f927a8ceb8e6
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_SSL_TRANSPORT_SECURITY_BINDING, WS_SSL_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows], _WS_SSL_TRANSPORT_SECURITY_BINDING, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING, wsw.ws_ssl_transport_security_binding
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_SSL_TRANSPORT_SECURITY_BINDING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SSL_TRANSPORT_SECURITY_BINDING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SSL_TRANSPORT_SECURITY_BINDING structure


## -description



The security binding subtype for specifying the use of SSL/TLS
protocol based transport security.
            


                This security binding is supported only with the
                <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
            


With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a> (client side only)
                    </li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_DISABLE_CERT_REVOCATION_CHECK</a> (client side only)                    
                    </li>
<li>
<a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_REQUIRE_SSL_CLIENT_CERT</a> (server side only)

</li>
</ul>



## -struct-fields




### -field binding


The base type from which this security binding subtype and all other security binding subtypes derive.
                


### -field localCertCredential


The local certificate credential to be used with this security binding.
                


Server side: When SSL is used for transport security with <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>, the server certificate must be
registered by the application using the httpcfg
tool and this field must be set to <b>NULL</b>.  In all other cases, the
server SSL certificate must be specified using this field.
                


Client side: If a client certificate is to be used with SSL, it must
be specified using this field.  If no client certificate is to be
used, this field must be set to <b>NULL</b>.
                

