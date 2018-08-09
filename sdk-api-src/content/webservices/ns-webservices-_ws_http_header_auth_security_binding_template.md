---
UID: NS:webservices._WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
title: "_WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE"
author: windows-sdk-content
description: The security binding template for specifying the use of HTP header authentication protocol based security.
old-location: wsw\ws_http_header_auth_security_binding_template.htm
old-project: wsw
ms.assetid: 4eabe380-de6d-48e3-bdad-dbf593a9850a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE, WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], _WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE, wsw.ws_http_header_auth_security_binding_template
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
req.typenames: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE structure


## -description


The security binding template for specifying the use of HTP header authentication 
        protocol based security.
      

See also <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>



## -struct-fields




### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.
        


### -field clientCredential

The Windows credential to be used to obtain this security token.  This
          is required on the client side and must be <b>NULL</b> on the server side.
        

