---
UID: NE:webservices.WS_SECURITY_BINDING_TYPE
title: WS_SECURITY_BINDING_TYPE
author: windows-sdk-content
description: The type of the security binding, used as a selector for subtypes of WS_SECURITY_BINDING.
old-location: wsw\ws_security_binding_type.htm
old-project: wsw
ms.assetid: caa3d71c-420c-4be0-a371-0f2d48ebd757
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE, WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, WS_SAML_MESSAGE_SECURITY_BINDING_TYPE, WS_SECURITY_BINDING_TYPE, WS_SECURITY_BINDING_TYPE enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE, WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE, WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE, webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_SAML_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_SECURITY_BINDING_TYPE, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE, wsw.ws_security_binding_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_SECURITY_BINDING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_BINDING_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_BINDING_TYPE enumeration


## -description


The type of the security binding, used as a selector for subtypes of
<a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">WS_SECURITY_BINDING</a>.  In general, the type name of the
security binding (one of the values defined here) specifies how the
security token used with that security binding is obtained and used.
            


## -enum-fields




### -field WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
                


### -field WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_SAML_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/713afe9a-49b8-419a-b78b-d3b5a4a8d073">WS_SAML_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE

Windows 8 or later:
Type id for the security binding <a href="https://msdn.microsoft.com/02FCD206-23BC-4ED0-9E4A-76AB0926FD7C">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                

