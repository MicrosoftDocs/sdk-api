---
UID: NS:webservices._WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
title: "_WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE"
author: windows-driver-content
description: The security binding template for specifying the use of Windows SSPI protocol based transport security. See also WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING.
old-location: wsw\ws_tcp_sspi_transport_security_binding_template.htm
old-project: wsw
ms.assetid: bdfd8bfe-a46d-4bbf-81e3-c0183fcd25bf
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], _WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE, wsw.ws_tcp_sspi_transport_security_binding_template
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
req.typenames: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure


## -description



        The security binding template for specifying the use of Windows SSPI
        protocol based transport security. 
      


        See also <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.
      


## -struct-fields




### -field securityBindingProperties


          Application provided security binding properties that cannot be represented in policy.
        


### -field clientCredential


          The Windows credential to be used to obtain this security token.  This
          is required on the client and must not be specified on the server.
        

