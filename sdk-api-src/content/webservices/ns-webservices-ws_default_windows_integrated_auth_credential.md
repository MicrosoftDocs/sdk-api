---
UID: NS:webservices._WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
title: WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL (webservices.h)
description: Type for supplying a Windows Integrated Authentication credential based on the current Windows identity.
helpviewer_keywords: ["WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL","WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows]","webservices/WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL","wsw.ws_default_windows_integrated_auth_credential"]
old-location: wsw\ws_default_windows_integrated_auth_credential.htm
tech.root: wsw
ms.assetid: 14753a2d-6054-4041-a72b-4cd7a9576f3b
ms.date: 12/05/2018
ms.keywords: WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows], webservices/WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, wsw.ws_default_windows_integrated_auth_credential
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
req.typenames: WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - webservices/_WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - webservices/WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
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
 - WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
---

# WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure


## -description

Type for supplying a Windows Integrated Authentication credential based on the current Windows identity. If this credential subtype is used for a security binding, the current thread token on the thread that calls <a href="/windows/desktop/api/webservices/nf-webservices-wsopenchannel">WsOpenChannel</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsopenserviceproxy">WsOpenServiceProxy</a> is used as the Windows identity when sending messages or making service calls.


<a href="/windows/desktop/api/webservices/nf-webservices-wsacceptchannel">WsAcceptChannel</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsopenservicehost">WsOpenServiceHost</a> do not support this credential type when called from an impersonating thread. 


This type derives from the base type <a href="/windows/win32/api/webservices/ns-webservices-ws_windows_integrated_auth_credential">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a>. For an instance of this type, the type selector field <b>credential.credentialType</b> must have the value <b>WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL_TYPE</b>.

## -struct-fields

### -field credential

The base type from which this type and all other Windows Integrated Authentication credential types derive.
                See <a href="/windows/win32/api/webservices/ns-webservices-ws_windows_integrated_auth_credential">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a>.