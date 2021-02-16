---
UID: NS:webservices._WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
title: WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL (webservices.h)
description: Type for supplying a Windows credential as username, password, domain strings.
helpviewer_keywords: ["WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL","WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows]","webservices/WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL","wsw.ws_string_windows_integrated_auth_credential"]
old-location: wsw\ws_string_windows_integrated_auth_credential.htm
tech.root: wsw
ms.assetid: 31a9c242-b56c-47d5-8b5a-a7a245575124
ms.date: 12/05/2018
ms.keywords: WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows], webservices/WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, wsw.ws_string_windows_integrated_auth_credential
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
req.typenames: WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - webservices/_WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - webservices/WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
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
 - WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
---

# WS_STRING_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure


## -description

Type for supplying a Windows credential as username, password, domain strings.

## -struct-fields

### -field credential

The base type from which this type and all other Windows Integrated
Authentication credential types derive.

### -field username

The username as a string.  This must be a valid user. To specify default credentials, use the WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL instead.

### -field password

The password for the username as a string.
                To specify a blank password, the length field of the string must be set to 0.

### -field domain

The domain name or the workgroup name as a string.

