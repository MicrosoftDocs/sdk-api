---
UID: NS:webservices._WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
title: WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE (webservices.h)
description: The type for specifying asymmetric cryptographic keys as a CryptoNG NCRYPT_KEY_HANDLE.
helpviewer_keywords: ["WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE","WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows]","webservices/WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE","wsw.ws_ncrypt_asymmetric_security_key_handle"]
old-location: wsw\ws_ncrypt_asymmetric_security_key_handle.htm
tech.root: wsw
ms.assetid: 843e8d93-3191-42e6-aa7b-d78b3b3370ec
ms.date: 12/05/2018
ms.keywords: WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE, WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows], webservices/WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE, wsw.ws_ncrypt_asymmetric_security_key_handle
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
req.typenames: WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
 - webservices/_WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
 - WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
 - webservices/WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
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
 - WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
---

# WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE structure


## -description

The type for specifying asymmetric cryptographic keys as a CryptoNG
NCRYPT_KEY_HANDLE.
            

When this structure is used in an API (such as with
 <a href="/windows/desktop/api/webservices/nf-webservices-wscreatexmlsecuritytoken">XML token creation</a>) and subsequent
<a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_token_message_security_binding">use of that XML
token</a> for a channel), the application is responsible for making
sure that the NCRYPT_KEY_HANDLE remains valid as long as the key is in
use.  The application is also responsible for freeing the handle when
it is no longer in use.
            

This type is supported only on Windows Vista and later platforms.

## -struct-fields

### -field keyHandle

The base type from which this type and all other key handle types derive.

### -field asymmetricKey

The CryptoNG asymmetric cryptographic key.