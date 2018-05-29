---
UID: NS:webservices._WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
title: "_WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION"
author: windows-sdk-content
description: Describes the policy specifying security context message binding over http channel binding, with SSL transport security. The bootstrap channel uses http channel binding with SSL transport security and KERBEROS AP_REQ message security.
old-location: wsw\ws_http_ssl_kerberos_apreq_security_context_policy_description.htm
old-project: wsw
ms.assetid: 2e228694-cfb1-48c5-a2c5-a0e57ad71724
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION, WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure [Web Services for Windows], _WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION, webservices/WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION, wsw.ws_http_ssl_kerberos_apreq_security_context_policy_description
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
req.typenames: WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION structure


## -description



        Describes the policy specifying security context message binding over http channel binding, with SSL 
        transport security. The bootstrap channel uses http channel binding with SSL transport security
        and KERBEROS AP_REQ message security.
      


## -struct-fields




### -field channelProperties


          Template description for the channel properties specified in policy.
        


### -field securityProperties


          Template description for the security properties specified in policy.
        


### -field sslTransportSecurityBinding


          SSL security binding description.
        


### -field kerberosApreqMessageSecurityBinding


          kerberos message security binding description.
        


### -field securityContextSecurityBinding


          Security context security binding description.
        

