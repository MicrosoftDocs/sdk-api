---
UID: NF:eaphostpeerconfigapis.EapHostPeerGetMethodProperties
title: EapHostPeerGetMethodProperties function
author: windows-sdk-content
description: Used to retrieve the properties of an EAP method given the connection and user data.
old-location: eaphost\eaphostpeergetmethodproperties.htm
tech.root: eaphost
ms.assetid: b553c022-c9a2-4cf7-8c09-e629b49cd929
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EapHostPeerGetMethodProperties, EapHostPeerGetMethodProperties function [EAPHost], eaphost.eaphostpeergetmethodproperties, eaphostpeerconfigapis/EapHostPeerGetMethodProperties
ms.topic: function
req.header: eaphostpeerconfigapis.h
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerGetMethodProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerGetMethodProperties function


## -description


The <b>EapHostPeerGetMethodProperties</b> function is used to retrieve the properties of an EAP method given the connection and user data.


## -parameters




### -param dwVersion [in]

The version number of the API. Set this parameter to zero.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the EAP authentication session behavior.
                


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that specifies the EAP method the supplicant is to use.


### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.


### -param dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pbEapConnData</i>.
                


### -param pbEapConnData [in]

Connection data used for the EAP method. If set to <b>NULL</b>, the static property of the method, as configured in the registry, is returned.


### -param dwUserDataSize [in]

The size, in bytes, of the user data buffer provided in <i>pbUserData</i>.
                


### -param pbUserData [in]

A pointer to a byte buffer that contains the opaque user data  BLOB. This parameter can be <b>NULL</b>.


### -param pMethodPropertyArray [out]

A pointer to the method properties array <a href="https://msdn.microsoft.com/1dfe2fb2-a4e5-4c14-8cde-083e45134f7b">EAP_METHOD_PROPERTY_ARRAY</a>. Caller should free the inner pointers using   <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a> starting
                at the innermost pointer. The caller should free an <b>empvString</b> value only when the type is <b>empvtString</b>.


### -param ppEapError [out]

 
A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeErrorMemory</a>.


## -remarks



<b>EapHostPeerGetMethodProperties</b> allows the user to retrieve the properties of an EAP method through the EAPHost supplicant interface. The properties returned by this API may be different from properties returned by the <a href="https://msdn.microsoft.com/5b2b351b-d6d8-406c-aa9f-ac720def3681">EapHostPeerGetMethods</a> function. The <b>EapHostPeerGetMethodProperties</b> function returns the properties of an EAP method for a specific connection and user data.




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>
 

 

