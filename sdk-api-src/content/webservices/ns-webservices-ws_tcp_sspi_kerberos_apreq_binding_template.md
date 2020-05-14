---
UID: NS:webservices._WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE
title: WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE (webservices.h)
description: Username/password security template information to be filled in by application. Associated with WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE.helpviewer_keywords: ["WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE","WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE","wsw.ws_tcp_sspi_kerberos_apreq_binding_template"]
old-location: wsw\ws_tcp_sspi_kerberos_apreq_binding_template.htm
tech.root: wsw
ms.assetid: 3856d462-baa3-49c7-8f14-f116d16efce0
ms.date: 12/05/2018
ms.keywords: WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE, WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE, wsw.ws_tcp_sspi_kerberos_apreq_binding_template
f1_keywords:
- webservices/WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE
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
- WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE
targetos: Windows
req.typenames: WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
---

# WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE structure


## -description


Username/password security template information to be filled in by application.
        Associated with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_binding_template_type">WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE</a>.
      


## -struct-fields




### -field channelProperties

Application provided additional channel properties that cannot be represented in policy.
        


### -field securityProperties

Application provided additional security properties that cannot be represented in policy.
        


### -field sspiTransportSecurityBinding

Application provided SSPI transport security information that cannot be represented
          in policy.
        


### -field kerberosApreqMessageSecurityBinding

Application provided kerberos binding information that cannot be represented in policy.
        

