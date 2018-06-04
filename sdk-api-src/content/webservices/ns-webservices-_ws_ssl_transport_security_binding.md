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
                

