---
UID: NF:eapmethodpeerapis.EapPeerQueryCredentialInputFields
title: EapPeerQueryCredentialInputFields function (eapmethodpeerapis.h)
author: windows-sdk-content
description: Defines the implementation of an EAP method-specific function that obtains the EAP Single-Sign-On (SSO) credential input fields for an EAP method.
old-location: eaphost\eappeerquerycredentialinputfields.htm
tech.root: eaphost
ms.assetid: 8ae42352-e972-4094-bf03-90a2f20ab641
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerQueryCredentialInputFields, EapPeerQueryCredentialInputFields function [EAPHost], eaphost.eappeerquerycredentialinputfields, eapmethodpeerapis/EapPeerQueryCredentialInputFields
ms.topic: function
req.header: eapmethodpeerapis.h
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
 - eapmethodpeerapis.h
api_name:
 - EapPeerQueryCredentialInputFields
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapPeerQueryCredentialInputFields function


## -description


Defines the implementation of an EAP method-specific function that obtains the EAP  Single-Sign-On (SSO) credential input fields for an EAP method.


## -parameters




### -param hUserImpersonationToken [in]

An impersonation token for the user whose credentials are to be requested and obtained.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwEapConnDataSize [in]

The size of the EAP SSO configuration byte data pointed to by <i>pbEapConnData</i>, in bytes.


### -param pbEapConnData [in]

A Pointer to an opaque byte buffer that contains the EAP configuration data BLOB.


### -param pEapConfigFieldsArray [out]

A Pointer to an <a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the input fields to display to the supplicant user. The <b>pwszData</b> fields in the individual <a href="https://msdn.microsoft.com/2b321f26-fb40-44e5-b483-52d85cb54c8c">EAP_CONFIG_INPUT_FIELD_DATA</a> elements are initialized to <b>NULL</b>.


### -param ppEapError [out]

 A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


## -remarks



<b>EapPeerQueryCredentialInputFields</b> supports SSO. This peer method function, like <a href="https://msdn.microsoft.com/bd4fafce-7ece-4cdc-9307-4d41538a4f49">EapPeerQueryUserBlobFromCredentialInputFields</a>, is used only in an SSO scenario.

 The EAP method-specific implementation of this function is called by EAPHost whenever a supplicant application calls <a href="https://msdn.microsoft.com/f71aad69-89f3-463b-afd7-9873d582d03b">EapHostPeerQueryCredentialInputFields</a>. The implementor of this function is responsible for ensuring that the  <a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a> returned by this function contains input field definitions for each piece of credential data the EAP methods will request from the supplicant user.




## -see-also




<a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

