---
UID: NS:webservices._WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
title: "_WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE"
author: windows-sdk-content
description: The type for specifying asymmetric cryptographic keys as CAPI 1.0 key handles.
old-location: wsw\ws_capi_asymmetric_security_key_handle.htm
old-project: wsw
ms.assetid: 1f5d1905-98ef-4481-88c7-4683cbeba0ae
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE, WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows], _WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE, webservices/WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE, wsw.ws_capi_asymmetric_security_key_handle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure


## -description


The type for specifying asymmetric cryptographic keys as CAPI 1.0 key
handles.
            

When this structure is used in an API (such as 
with <a href="https://msdn.microsoft.com/1d82c6c3-2bcf-4883-aed7-1a163bbb2228">XML token creation</a> and subsequent
<a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">use of that XML
token</a> for a channel), the application is responsible for making
sure that the HCRYPTPROV remains valid as long as the key is in
use.  The application is also responsible for freeing the handle when
it is no longer in use.
            

This type is supported only on pre-Windows Vista platforms: for
Windows Vista and later, please use <a href="https://msdn.microsoft.com/843e8d93-3191-42e6-aa7b-d78b3b3370ec">WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE</a>.
            


## -struct-fields




### -field keyHandle

The base type from which this type and all other key handle types derive.
                


### -field provider

The cryptographic provider.
                


### -field keySpec

The key specification.
                

