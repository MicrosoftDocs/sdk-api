---
UID: NE:webservices.__unnamed_enum_47
title: WS_SECURITY_BINDING_TYPE
author: windows-sdk-content
description: The type of the security binding, used as a selector for subtypes of WS_SECURITY_BINDING.
old-location: wsw\ws_security_binding_type.htm
tech.root: wsw
ms.assetid: caa3d71c-420c-4be0-a371-0f2d48ebd757
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE, WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, WS_SAML_MESSAGE_SECURITY_BINDING_TYPE, WS_SECURITY_BINDING_TYPE, WS_SECURITY_BINDING_TYPE enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE, WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE, WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE, webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_SAML_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_SECURITY_BINDING_TYPE, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE, wsw.ws_security_binding_type
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
 - WS_SECURITY_BINDING_TYPE
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_BINDING_TYPE
req.redist: 
---

# WS_SECURITY_BINDING_TYPE enumeration


## -description


The type of the security binding, used as a selector for subtypes of
<a href="https://msdn.microsoft.com/6c0663e8-ae73-41a2-9273-50f53534926b">WS_SECURITY_BINDING</a>.  In general, the type name of the
security binding (one of the values defined here) specifies how the
security token used with that security binding is obtained and used.
            


## -enum-fields




### -field WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd323441(v=VS.85).aspx">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd323466(v=VS.85).aspx">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                


### -field WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd401908(v=VS.85).aspx">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
                


### -field WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd323497(v=VS.85).aspx">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd401944(v=VS.85).aspx">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd323568(v=VS.85).aspx">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_SAML_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd323373(v=VS.85).aspx">WS_SAML_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE

Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Dd323391(v=VS.85).aspx">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>.
                


### -field WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE

Windows 8 or later:
Type id for the security binding <a href="https://msdn.microsoft.com/en-us/library/Hh437361(v=VS.85).aspx">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>.
                

