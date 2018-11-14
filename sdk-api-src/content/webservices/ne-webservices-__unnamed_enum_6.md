---
UID: NE:webservices.__unnamed_enum_6
title: "__unnamed_enum_6"
author: windows-sdk-content
description: Defines the options for performing client authentication using HTTP authentication headers.
old-location: wsw\ws_http_header_auth_scheme.htm
tech.root: wsw
ms.assetid: c96e10ee-29d1-4c66-9f4d-64e663b25fd0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SCHEME, WS_HTTP_HEADER_AUTH_SCHEME enumeration [Web Services for Windows], WS_HTTP_HEADER_AUTH_SCHEME_BASIC, WS_HTTP_HEADER_AUTH_SCHEME_DIGEST, WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE, WS_HTTP_HEADER_AUTH_SCHEME_NONE, WS_HTTP_HEADER_AUTH_SCHEME_NTLM, WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT, __unnamed_enum_6, webservices/WS_HTTP_HEADER_AUTH_SCHEME, webservices/WS_HTTP_HEADER_AUTH_SCHEME_BASIC, webservices/WS_HTTP_HEADER_AUTH_SCHEME_DIGEST, webservices/WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE, webservices/WS_HTTP_HEADER_AUTH_SCHEME_NONE, webservices/WS_HTTP_HEADER_AUTH_SCHEME_NTLM, webservices/WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT, wsw.ws_http_header_auth_scheme
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - WS_HTTP_HEADER_AUTH_SCHEME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_6 enumeration


## -description


Defines the options for performing client authentication using HTTP
authentication headers.
            


## -enum-fields




### -field WS_HTTP_HEADER_AUTH_SCHEME_NONE

No authentication is required. This value is only supported on the client.
            


### -field WS_HTTP_HEADER_AUTH_SCHEME_BASIC

HTTP basic authentication as defined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=139705">RFC 2617</a>.
                


### -field WS_HTTP_HEADER_AUTH_SCHEME_DIGEST

HTTP digest authentication as defined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=139705">RFC 2617</a>.
                


### -field WS_HTTP_HEADER_AUTH_SCHEME_NTLM

Authentication done by carrying NTLM packets in HTTP authentication
headers as defined in <a href=" http://go.microsoft.com/fwlink/p/?linkid=139705">RFC 2617</a>.
                


### -field WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE

Authentication done by carrying SPNEGO packets in HTTP authentication
headers as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=139707">RFC
4559</a>.
                


### -field WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT

Authentication done by using Microsoft Passport 1.4 authentication protocol. This value is only supported on the client for legacy purposes. 
This value is not supported on Windows Server 2008 R2and later.
                

