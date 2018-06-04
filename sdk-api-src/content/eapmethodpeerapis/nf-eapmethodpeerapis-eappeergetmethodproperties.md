---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EapPeerGetMethodProperties function


## -description


Defines the implementation of an EAP method-specific function that retrieves the properties of an EAP method given the connection and user data.


## -parameters




### -param dwVersion [in]

The version number of the API.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the EAP authentication session behavior.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that identifies the EAP method the supplicant is to use.


### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.


### -param dwSizeOfConnectionDataIn

TBD


### -param pConnectionDataIn

TBD


### -param dwSizeOfUserDataIn

TBD


### -param pUserDataIn

TBD


### -param pMethodPropertyArray [out]

A pointer to the method properties array <a href="https://msdn.microsoft.com/1dfe2fb2-a4e5-4c14-8cde-083e45134f7b">EAP_METHOD_PROPERTY_ARRAY</a>. Caller should free the inner pointers using <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a> starting
                at the innermost pointer. The caller should free an <b>empvString</b> value only when the type is <b>empvtString</b>.


### -param ppEapError [out]

 
A pointer to a address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapPeerFreeErrorMemory</a>.


#### - dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pbEapConnData</i>.


#### - dwUserDataSize [in]

The size, in bytes, of the user data buffer provided in <i>pbUserData</i>.
                


#### - pbEapConnData [in]

Connection data used for the EAP method. If set to NULL, the static property of the method, as configured in the registry, is returned.


#### - pbUserData [in]

A pointer to a byte buffer that contains the opaque user data  BLOB. This parameter can be NULL.

