---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryUserBlobFromCredentialInputFields
title: EapHostPeerQueryUserBlobFromCredentialInputFields function
author: windows-sdk-content
description: Obtains a credential BLOB that can be used to start authentication from user input received from the Single-Sign-On (SSO) UI.
old-location: eaphost\eaphostpeerqueryuserblobfromcredentialinputfields.htm
tech.root: EAPHost
ms.assetid: bd4fafce-7ece-4cdc-9307-4d41538a4f49
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EapHostPeerQueryUserBlobFromCredentialInputFields, EapHostPeerQueryUserBlobFromCredentialInputFields function [EAPHost], eaphost.eaphostpeerqueryuserblobfromcredentialinputfields, eaphostpeerconfigapis/EapHostPeerQueryUserBlobFromCredentialInputFields
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EapHostPeerQueryUserBlobFromCredentialInputFields
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerQueryUserBlobFromCredentialInputFields function


## -description


The <b>EapHostPeerQueryUserBlobFromCredentialInputFields</b> function obtains
a credential BLOB that can be used to start authentication from user input received from the Single-Sign-On (SSO) UI.


## -parameters




### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pConnectionData.</i>


### -param pbEapConnData [in]

Connection data used for the EAP method.


### -param pEapConfigInputFieldArray [in]

A pointer  to an <a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure the contains the UI input field data. The caller should free the inner pointers
                using the function <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting at the innermost pointer.


### -param pdwUserBlobSize [in, out]

A pointer to a DWORD that specifies the size, in bytes, of the buffer pointed to by <i>ppbUserBlob</i>. If this value is not set to zero, then a pointer to a buffer of the size specified in this parameter must be supplied to <i>ppbUserBlob</i>.


### -param ppbUserBlob [in, out]

A pointer to the credential BLOB that can be used in authentication.
                Memory must be freed by calling <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>. If a non-null value is supplied for this parameter (meaning that an existing data BLOB is passed to it), the supplied data BLOB will be updated and returned in this parameter.  If a non-NULL BLOB value is supplied, the <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function should be used. 


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


## -remarks



<b>EapHostPeerQueryUserBlobFromCredentialInputFields</b> supports SSO. This supplicant function, like <a href="https://msdn.microsoft.com/f71aad69-89f3-463b-afd7-9873d582d03b">EapHostPeerQueryCredentialInputFields</a>, is used only in an SSO scenario.

After <b>EapHostPeerQueryUserBlobFromCredentialInputFields</b>, EAPHost calls <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>. The supplicant  uses the <b>EAP_FLAG_PRE_LOGON</b> flag in <b>EapHostPeerBeginSession</b> to indicate that EAPHost should provide SSO. 




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

