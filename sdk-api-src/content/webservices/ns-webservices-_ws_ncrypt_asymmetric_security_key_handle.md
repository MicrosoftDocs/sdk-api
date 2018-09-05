---
UID: NS:webservices._WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
title: "_WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE"
author: windows-sdk-content
description: The type for specifying asymmetric cryptographic keys as a CryptoNG NCRYPT_KEY_HANDLE.
old-location: wsw\ws_ncrypt_asymmetric_security_key_handle.htm
old-project: wsw
ms.assetid: 843e8d93-3191-42e6-aa7b-d78b3b3370ec
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE, WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows], _WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE, webservices/WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE, wsw.ws_ncrypt_asymmetric_security_key_handle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.redist: 
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
req.typenames: WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE structure


## -description


The type for specifying asymmetric cryptographic keys as a CryptoNG
NCRYPT_KEY_HANDLE.
            

When this structure is used in an API (such as with
 <a href="https://msdn.microsoft.com/1d82c6c3-2bcf-4883-aed7-1a163bbb2228">XML token creation</a>) and subsequent
<a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">use of that XML
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
                

