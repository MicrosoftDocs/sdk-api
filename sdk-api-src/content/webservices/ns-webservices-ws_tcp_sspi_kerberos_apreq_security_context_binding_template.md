---
UID: NS:webservices._WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
title: WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE (webservices.h)
description: Security template information to be filled in by application. Associated with WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE.
helpviewer_keywords: ["WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE","WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE","wsw.ws_tcp_sspi_kerberos_apreq_security_context_binding_template"]
old-location: wsw\ws_tcp_sspi_kerberos_apreq_security_context_binding_template.htm
tech.root: wsw
ms.assetid: 2499125c-757c-4960-a1b6-aa41c55e7594
ms.date: 12/05/2018
ms.keywords: WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE, WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE, wsw.ws_tcp_sspi_kerberos_apreq_security_context_binding_template
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
targetos: Windows
req.typenames: WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
 - webservices/_WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
 - WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
 - webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
---

# WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure


## -description

Security template information to be filled in by application.
        Associated with <a href="/windows/desktop/api/webservices/ne-webservices-ws_binding_template_type">WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</a>.

## -struct-fields

### -field channelProperties

Application provided additional channel properties for both bootstrap channel and service channel
          that cannot be represented in policy.

### -field securityProperties

Application provided additional security properties for the bootstrap channel 
          that cannot be represented in policy.

### -field sspiTransportSecurityBinding

Application provided SSPI transport security information for the bootstrap channel and service 
          channel that cannot be represented in policy.

### -field kerberosApreqMessageSecurityBinding

Application provided kerberos binding information for the bootstrap channel that cannot be represented in policy.

### -field securityContextSecurityBinding

Application provided security context message binding information for the service channel that cannot be represented in policy.