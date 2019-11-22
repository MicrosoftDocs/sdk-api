---
UID: NS:webservices._WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
title: WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE (webservices.h)

description: Security template information to be filled in by application. Associated with WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE.
old-location: wsw\ws_http_ssl_kerberos_apreq_security_context_binding_template.htm
tech.root: wsw
ms.assetid: ac896c5c-9784-4f89-bdd8-8b6d2136c416

ms.date: 12/05/2018
ms.keywords: WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE, WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE, wsw.ws_http_ssl_kerberos_apreq_security_context_binding_template
ms.topic: struct
f1_keywords: 
 - "webservices/WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE"
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
 - WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
targetos: Windows
req.typenames: WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
---

# WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure


## -description


Security template information to be filled in by application.
        Associated with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_binding_template_type">WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</a>.
      


## -struct-fields




### -field channelProperties

Application provided additional channel properties for both bootstrap channel and service channel
          that cannot be represented in policy.
        


### -field securityProperties

Application provided additional security properties for the bootstrap channel that cannot be represented in policy.
        


### -field sslTransportSecurityBinding

Application provided SSL transport security binding information for both bootstrap channel and
          service channel that cannot be represented
          in policy.
        


### -field kerberosApreqMessageSecurityBinding

Application provided username binding information for the bootstrap channel that cannot be represented in policy.
        


### -field securityContextSecurityBinding

Application provided security context message binding information for the service channel that cannot be represented in policy.
        

