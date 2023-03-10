---
UID: NS:webservices._WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
title: WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE (webservices.h)
description: The type for specifying asymmetric cryptographic keys as CAPI 1.0 key handles.
helpviewer_keywords: ["WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE","WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows]","webservices/WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE","wsw.ws_capi_asymmetric_security_key_handle"]
old-location: wsw\ws_capi_asymmetric_security_key_handle.htm
tech.root: wsw
ms.assetid: 1f5d1905-98ef-4481-88c7-4683cbeba0ae
ms.date: 12/05/2018
ms.keywords: WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE, WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows], webservices/WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE, wsw.ws_capi_asymmetric_security_key_handle
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
req.typenames: WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
 - webservices/_WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
 - WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
 - webservices/WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
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
 - WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
---

# WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure


## -description

The type for specifying asymmetric cryptographic keys as CAPI 1.0 key
handles.
            

When this structure is used in an API (such as 
with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatexmlsecuritytoken">XML token creation</a> and subsequent
<a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_token_message_security_binding">use of that XML
token</a> for a channel), the application is responsible for making
sure that the HCRYPTPROV remains valid as long as the key is in
use.  The application is also responsible for freeing the handle when
it is no longer in use.
            

This type is supported only on pre-Windows Vista platforms: for
Windows Vista and later, please use <a href="/windows/win32/api/webservices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle">WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE</a>.

## -struct-fields

### -field keyHandle

The base type from which this type and all other key handle types derive.

### -field provider

The cryptographic provider.

### -field keySpec

The key specification.