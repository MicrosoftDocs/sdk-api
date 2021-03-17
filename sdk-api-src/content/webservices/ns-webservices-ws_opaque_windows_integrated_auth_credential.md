---
UID: NS:webservices._WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
title: WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL (webservices.h)
description: Type for supplying a Windows Integrated Authentication credential as an opaque handle created by SspiPromptForCredentials and the related family of APIs. This feature is available only on Windows 7 and later.
helpviewer_keywords: ["WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL","WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows]","webservices/WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL","wsw.ws_opaque_windows_integrated_auth_credential"]
old-location: wsw\ws_opaque_windows_integrated_auth_credential.htm
tech.root: wsw
ms.assetid: 9dc8bde7-b70d-4b1f-9b3f-41af9ea7f215
ms.date: 12/05/2018
ms.keywords: WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure [Web Services for Windows], webservices/WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL, wsw.ws_opaque_windows_integrated_auth_credential
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
req.typenames: WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - webservices/_WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
 - webservices/WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
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
 - WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL
---

# WS_OPAQUE_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure


## -description

Type for supplying a Windows Integrated Authentication credential as an opaque handle created by
SspiPromptForCredentials and the related family of APIs.  This feature
is available only on Windows 7 and later.

## -struct-fields

### -field credential

The base type from which this type and all other Windows Integrated Authentication credential types derive.

### -field opaqueAuthIdentity

The opaque form of authentication identity. The supplied value must be of the type PSEC_WINNT_AUTH_IDENTITY_OPAQUE.

