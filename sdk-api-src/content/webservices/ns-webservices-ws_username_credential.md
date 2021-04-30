---
UID: NS:webservices._WS_USERNAME_CREDENTIAL
title: WS_USERNAME_CREDENTIAL (webservices.h)
description: The abstract base type for all username/password credentials.
helpviewer_keywords: ["WS_USERNAME_CREDENTIAL","WS_USERNAME_CREDENTIAL structure [Web Services for Windows]","webservices/WS_USERNAME_CREDENTIAL","wsw.ws_username_credential"]
old-location: wsw\ws_username_credential.htm
tech.root: wsw
ms.assetid: 961f8c52-9922-4e43-905a-a22a80aba63b
ms.date: 12/05/2018
ms.keywords: WS_USERNAME_CREDENTIAL, WS_USERNAME_CREDENTIAL structure [Web Services for Windows], webservices/WS_USERNAME_CREDENTIAL, wsw.ws_username_credential
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
req.typenames: WS_USERNAME_CREDENTIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_USERNAME_CREDENTIAL
 - webservices/_WS_USERNAME_CREDENTIAL
 - WS_USERNAME_CREDENTIAL
 - webservices/WS_USERNAME_CREDENTIAL
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
 - WS_USERNAME_CREDENTIAL
---

# WS_USERNAME_CREDENTIAL structure


## -description

The abstract base type for all username/password credentials.
            

Note that <b>WS_USERNAME_CREDENTIAL</b> and its concrete subtypes
are used with the WS-Security <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.  
They are best suitable for application-level username/password pairs, such as 
those used for online customer accounts.  The usernames and passwords specified 
are not interpreted by the security runtime, and are merely carried
client-to-server for authentication by the specified server-side
username/password validator specified by the application.
            

In contrast, the <a href="/windows/win32/api/webservices/ns-webservices-ws_windows_integrated_auth_credential">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> and
its concrete subtypes are used for Windows Integrated Authentication
and the security bindings that use it.

## -struct-fields

### -field credentialType

The selector for the type of the username credential.