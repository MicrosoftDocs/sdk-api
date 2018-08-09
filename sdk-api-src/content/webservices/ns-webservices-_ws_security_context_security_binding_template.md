---
UID: NS:webservices._WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE
title: "_WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE"
author: windows-sdk-content
description: The security binding template for specifying the use of an application supplied security context security binding.
old-location: wsw\ws_security_context_security_binding_template.htm
old-project: wsw
ms.assetid: 09b6be85-ec60-4ba9-857f-fffc1f5fb368
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE, WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], _WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE, webservices/WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE, wsw.ws_security_context_security_binding_template
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
req.typenames: WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE structure


## -description


The security binding template for specifying the use of an application
        supplied security context security binding.  This security binding may 
        be used only with message security. So, it is used in conjunction with another transport
        security binding that provides message protection. The security properties are 
        used to establish the secure conversation.
      

See also <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>



## -struct-fields




### -field securityContextMessageSecurityBinding

Application provided security binding properties that cannot be represented in policy.
        


### -field securityProperties

Application provided additional security properties for the service channel
          that cannot be represented in policy. Only policy specified security properties is used if no additional properties are specified here.
        

