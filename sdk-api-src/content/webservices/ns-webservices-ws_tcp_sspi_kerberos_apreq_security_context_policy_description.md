---
UID: NS:webservices._WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
title: WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION (webservices.h)
description: Describes the policy specifying security context message binding using TCP channel binding with windows SSPI transport security. The bootstrap channel uses TCP channel binding with windows SSPI transport security and kerberos message security.
helpviewer_keywords: ["WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION","WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure [Web Services for Windows]","webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION","wsw.ws_tcp_sspi_kerberos_apreq_security_context_policy_description"]
old-location: wsw\ws_tcp_sspi_kerberos_apreq_security_context_policy_description.htm
tech.root: wsw
ms.assetid: 8bf8ffe4-f812-4d72-80d2-f15339e4b6b5
ms.date: 12/05/2018
ms.keywords: WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION, WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure [Web Services for Windows], webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION, wsw.ws_tcp_sspi_kerberos_apreq_security_context_policy_description
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
req.typenames: WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
 - webservices/_WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
 - WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
 - webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
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
 - WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
---

# WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure


## -description

Describes the policy specifying security context message binding using TCP channel binding 
        with windows SSPI transport security. The bootstrap channel uses TCP channel binding with 
        windows SSPI transport security and kerberos message security.

## -struct-fields

### -field channelProperties

Template description for the channel properties specified in policy.

### -field securityProperties

Template description for the security properties specified in policy.

### -field sspiTransportSecurityBinding

Windows SSPI security binding description.

### -field kerberosApreqMessageSecurityBinding

kerberos message security binding description.

### -field securityContextSecurityBinding

Security context security binding description.

