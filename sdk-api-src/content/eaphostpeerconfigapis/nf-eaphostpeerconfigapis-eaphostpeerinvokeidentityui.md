---
UID: NF:eaphostpeerconfigapis.EapHostPeerInvokeIdentityUI
title: EapHostPeerInvokeIdentityUI function
author: windows-sdk-content
description: This function is called by tunnel methods to invoke the identity UI of the inner methods. This function returns the identity as well as credentials to use in order to start the authentication.
old-location: eaphost\eaphostpeerinvokeidentityui.htm
old-project: EAPHost
ms.assetid: 48c48162-44d8-45d2-9147-5bf006d493b5
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapHostPeerInvokeIdentityUI, EapHostPeerInvokeIdentityUI function [EAPHost], eaphost.eaphostpeerinvokeidentityui, eaphostpeerconfigapis/EapHostPeerInvokeIdentityUI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: eaphostpeerconfigapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EAP_AUTHENTICATOR_SEND_TIMEOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	eappcfg.dll
api_name:
-	EapHostPeerInvokeIdentityUI
product: Windows
targetos: Windows
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerInvokeIdentityUI function


## -description


This function is called by tunnel methods to invoke the identity UI of the inner methods. This function returns the identity as well as credentials to use in order to start the authentication.


## -parameters




### -param dwVersion [in]

The version number of the API. Must be set to zero.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param hwndParent [in]

Handle of the parent window under which the configuration dialog will show up.


### -param dwSizeofConnectionData [in]

Size of the buffer indicated by the <i>pConnectionData</i> parameter, in bytes.


### -param pConnectionData [in]

Pointer to configuration data that is used for the EAP method.


### -param dwSizeofUserData [in]

Size of the buffer indicated by the <i>pUserData</i> parameter, in bytes.


### -param pUserData [in]

Pointer to user credential information that pertains to this authentication.


### -param pdwSizeOfUserDataOut

TBD


### -param ppUserDataOut [out]

A pointer to a pointer to a buffer that contains user data information returned by the method. After use, this memory must be freed by calling <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>.


### -param ppwszIdentity [out]

A pointer to a NULL-terminated user identity string. After use, this memory must be freed by calling  <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>. 



### -param ppvReserved [in, out]

Reserved for future use.


#### - pdwSizeofUserDataOut [in, out]

Size of the buffer set to receive the user data returned by the <i>ppUserDataOut</i> parameter, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>
 

 

