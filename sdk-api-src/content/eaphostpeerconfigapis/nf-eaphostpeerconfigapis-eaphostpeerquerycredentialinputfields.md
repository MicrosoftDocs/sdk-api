---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryCredentialInputFields
title: EapHostPeerQueryCredentialInputFields function
author: windows-sdk-content
description: Allows the user to determine what kind of credentials are required by the methods to perform authentication in a Single-Sign-On (SSO) scenario.
old-location: eaphost\eaphostpeerquerycredentialinputfields.htm
old-project: EAPHost
ms.assetid: f71aad69-89f3-463b-afd7-9873d582d03b
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapHostPeerQueryCredentialInputFields, EapHostPeerQueryCredentialInputFields function [EAPHost], eaphost.eaphostpeerquerycredentialinputfields, eaphostpeerconfigapis/EapHostPeerQueryCredentialInputFields
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
-	EapHostPeerQueryCredentialInputFields
product: Windows
targetos: Windows
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerQueryCredentialInputFields function


## -description


Allows the user to determine what kind of credentials are required by the methods  to perform authentication  in a Single-Sign-On (SSO) scenario.


## -parameters




### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that identifies the EAP method the supplicant is to use. 


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pbEapConnData.</i>


### -param pbEapConnData [in]

Connection data used for the EAP method. 


### -param pEapConfigInputFieldArray [out]

A pointer  to an <a href="https://msdn.microsoft.com/a3e2d5c0-eacd-46de-b092-6fd749870881">EAP_METHOD_INFO_ARRAY</a> structure for installed EAP methods. The caller should free the inner pointers
                using the function <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting at the innermost pointer.


### -param ppEapError

TBD




#### - pEapError [out]

 
A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


## -remarks



<b>EapHostPeerQueryCredentialInputFields</b> supports Single-Sign-On (SSO).  This supplicant function, like <a href="https://msdn.microsoft.com/decfe3cd-642e-41c8-9bec-d079a0f74504">EapHostPeerQueryUserBlobFromCredentialInputFields</a>, is used only in an SSO scenario.

<b>EapHostPeerQueryCredentialInputFields</b> obtains the fields to be displayed in the UI during the session. The input fields are obtained to display data entered by the user in the SSO UI. The <a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure returned contains details on how to display the input fields.

After <b>EapHostPeerQueryCredentialInputFields</b>, EAPHost calls <a href="https://msdn.microsoft.com/bd4fafce-7ece-4cdc-9307-4d41538a4f49">EapHostPeerQueryUserBlobFromCredentialInputFields</a>.




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

