---
UID: NS:eapauthenticatoractiondefine._EAP_METHOD_AUTHENTICATOR_RESULT
title: "_EAP_METHOD_AUTHENTICATOR_RESULT"
author: windows-sdk-content
description: Contains authentication results returned by an EAP authenticator method.
old-location: eaphost\eap_method_authenticator_result.htm
tech.root: eaphost
ms.assetid: 8367fd35-852b-4cdf-9a86-7d07a5a1a2ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EAP_METHOD_AUTHENTICATOR_RESULT, EAP_METHOD_AUTHENTICATOR_RESULT structure [EAPHost], _EAP_METHOD_AUTHENTICATOR_RESULT, eapauthenticatoractiondefine/EAP_METHOD_AUTHENTICATOR_RESULT, eaphost.eap_method_authenticator_result
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eapauthenticatoractiondefine.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapAuthenticatorActionDefine.h
api_name:
 - EAP_METHOD_AUTHENTICATOR_RESULT
product: Windows
targetos: Windows
req.typenames: EAP_METHOD_AUTHENTICATOR_RESULT
req.redist: 
---

# _EAP_METHOD_AUTHENTICATOR_RESULT structure


## -description


Contains authentication results returned by an EAP authenticator method.


## -struct-fields




### -field fIsSuccess

If <b>TRUE</b>, the supplicant was successfully authenticated; if <b>FALSE</b>, it was not.


### -field dwFailureReason

Contains a reason code if the supplicant could not be authenticated. Reason codes are generally expected to originate from winerror.h.


### -field pAuthAttribs

A pointer to an <a href="https://msdn.microsoft.com/2f88b475-a4ae-4c40-b0f8-2dd05c676619">EAP_ATTRIBUTES</a> structure that contains the EAP attributes  returned by the authentication session.


## -see-also




<a href="https://msdn.microsoft.com/e26d5db7-f247-4bff-ae5f-081474f8e61e">EAPHost Authenticator Method Structures</a>
 

 

