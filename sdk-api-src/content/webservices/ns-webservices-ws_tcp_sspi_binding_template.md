---
UID: NS:webservices._WS_TCP_SSPI_BINDING_TEMPLATE
title: WS_TCP_SSPI_BINDING_TEMPLATE (webservices.h)
author: windows-sdk-content
description: HTTP header authentication security template information to be filled in by application. Associated with WS_TCP_SSPI_BINDING_TEMPLATE_TYPE.
old-location: wsw\ws_tcp_sspi_binding_template.htm
tech.root: wsw
ms.assetid: d81a71fa-4743-4831-8863-a8fa73d4a9f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_TCP_SSPI_BINDING_TEMPLATE, WS_TCP_SSPI_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_TCP_SSPI_BINDING_TEMPLATE, wsw.ws_tcp_sspi_binding_template
ms.topic: struct
f1_keywords: 
 - "webservices/WS_TCP_SSPI_BINDING_TEMPLATE"
dev_langs:
 - c++
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
 - WS_TCP_SSPI_BINDING_TEMPLATE
targetos: Windows
req.typenames: WS_TCP_SSPI_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
---

# WS_TCP_SSPI_BINDING_TEMPLATE structure


## -description


HTTP header authentication security template information to be filled in by application.
        Associated with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_binding_template_type">WS_TCP_SSPI_BINDING_TEMPLATE_TYPE</a>.
      


## -struct-fields




### -field channelProperties

Application provided additional channel properties that cannot be represented in policy.
        


### -field securityProperties

Application provided additional security properties that cannot be represented in policy.
        


### -field sspiTransportSecurityBinding

Application provided SSPI transport security information that cannot be represented
          in policy.
        

