---
UID: NS:webservices._WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
title: "_WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE"
author: windows-driver-content
description: The security binding template for specifying the use of SSL/TLS protocol based transport security. See also WS_SSL_TRANSPORT_SECURITY_BINDING .This security binding is supported only with the WS_HTTP_CHANNEL_BINDING.
old-location: wsw\ws_ssl_transport_security_binding_template.htm
old-project: wsw
ms.assetid: 6b7e9ed6-0337-479d-9a83-dec5770c050d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE, WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], _WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE, wsw.ws_ssl_transport_security_binding_template
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
req.typenames: WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE structure


## -description



        The security binding template for specifying the use of SSL/TLS
        protocol based transport security. 
      

See also <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>
      .

This security binding is supported only with the
        <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
      


## -struct-fields




### -field securityBindingProperties


          Application provided security binding properties that cannot be represented in policy.
        


### -field localCertCredential


          The local certificate credential to be used with this security binding.
        


          Server side: When SSL is used for transport security with <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>, the server certificate must be
          registered by the application using the <a href="http://go.microsoft.com/fwlink/p/?linkid=95010">HttpCfg.exe</a> and this field must be set to <b>NULL</b>.  In all other cases, the
          server SSL certificate must be specified using this field.
        


          Client side: If a client certificate is to be used with SSL, it must
          be specified using this field.  If no client certificate is to be
          used, this field must be set to <b>NULL</b>.
        

