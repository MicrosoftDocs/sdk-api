---
UID: NE:webservices.__unnamed_enum_109
title: WS_BINDING_TEMPLATE_TYPE
author: windows-sdk-content
description: An enumeration of the different security binding combinations that are supported.
old-location: wsw\ws_binding_template_type.htm
tech.root: wsw
ms.assetid: 831001f4-619d-4128-a645-85077701c28c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_BINDING_TEMPLATE_TYPE, WS_BINDING_TEMPLATE_TYPE enumeration [Web Services for Windows], WS_HTTP_BINDING_TEMPLATE_TYPE, WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, WS_TCP_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, wsw.ws_binding_template_type
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
 - WS_BINDING_TEMPLATE_TYPE
product: Windows
targetos: Windows
req.typenames: WS_BINDING_TEMPLATE_TYPE
req.redist: 
---

# WS_BINDING_TEMPLATE_TYPE enumeration


## -description


An enumeration of the different security binding combinations that 
        are supported.


## -enum-fields




### -field WS_HTTP_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding. 
        


### -field WS_HTTP_SSL_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.
        


### -field WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>



### -field WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.
        


### -field WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> 
          and <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.
        


### -field WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
        


### -field WS_TCP_BINDING_TEMPLATE_TYPE

The policy specifies TCP channel binding.
        


### -field WS_TCP_SSPI_BINDING_TEMPLATE_TYPE

The policy specifies TCP channel binding with <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.
        


### -field WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE

The policy specifies TCP channel binding with <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.
        


### -field WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE

The policy specifies TCP channel binding with <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
      


### -field WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with HTTP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.
        


### -field WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE

The policy specifies HTTP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with HTTP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
        


### -field WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE

The policy specifies TCP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with TCP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.
        


### -field WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE

The policy specifies TCP channel binding with <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with TCP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
        

