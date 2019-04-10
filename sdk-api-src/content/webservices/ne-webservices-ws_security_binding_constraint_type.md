---
UID: NE:webservices.__unnamed_enum_107
title: WS_SECURITY_BINDING_CONSTRAINT_TYPE (webservices.h)
author: windows-sdk-content
description: The values in this enumeration are used to identify the sub-types of WS_SECURITY_BINDING_CONSTRAINT.
old-location: wsw\ws_security_binding_constraint_type.htm
tech.root: wsw
ms.assetid: 198869b4-0f25-4f10-8740-e4d501f6791b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE, WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, wsw.ws_security_binding_constraint_type
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
 - WS_SECURITY_BINDING_CONSTRAINT_TYPE
product: Windows
targetos: Windows
req.typenames: WS_SECURITY_BINDING_CONSTRAINT_TYPE
req.redist: 
---

# WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration


## -description


The values in this enumeration are used to identify the sub-types of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>.
            


## -enum-fields




### -field WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd323442(v=VS.85).aspx">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd323467(v=VS.85).aspx">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd401909(v=VS.85).aspx">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd323498(v=VS.85).aspx">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd401945(v=VS.85).aspx">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd401941(v=VS.85).aspx">WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd401776(v=VS.85).aspx">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/en-us/library/Dd323381(v=VS.85).aspx">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/en-us/library/Dd323392(v=VS.85).aspx">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
               

