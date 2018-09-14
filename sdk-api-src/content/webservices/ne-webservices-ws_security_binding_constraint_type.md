---
UID: NE:webservices.WS_SECURITY_BINDING_CONSTRAINT_TYPE
title: WS_SECURITY_BINDING_CONSTRAINT_TYPE
author: windows-sdk-content
description: The values in this enumeration are used to identify the sub-types of WS_SECURITY_BINDING_CONSTRAINT.
old-location: wsw\ws_security_binding_constraint_type.htm
tech.root: wsw
ms.assetid: 198869b4-0f25-4f10-8740-e4d501f6791b
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE, WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, wsw.ws_security_binding_constraint_type
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


The values in this enumeration are used to identify the sub-types of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>.
            


## -enum-fields




### -field WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/1f547d95-0a9a-44c5-81db-b92880238b1d">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/c2e793dd-99a7-4028-9e08-4376d494e2b5">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/1f6341b2-1f98-40a0-8f3a-cc9cf4538209">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/a3003b9c-405e-4b3d-89a4-6c0884c28805">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/fd422ee4-64cd-464f-905f-b46b69e1a440">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/7588f526-d1d5-486f-b317-f1a4b35e3882">WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/81f42654-8f94-4231-a798-67fbbe46e812">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
                


### -field WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE

This value is used in the type field of <a href="https://msdn.microsoft.com/d79795ea-6780-4d13-9d40-bd1ea7cd5113">WS_SECURITY_BINDING_CONSTRAINT</a>to identify a <a href="https://msdn.microsoft.com/7abc37d8-cb00-459d-aa08-609a06b65a5c">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
               

