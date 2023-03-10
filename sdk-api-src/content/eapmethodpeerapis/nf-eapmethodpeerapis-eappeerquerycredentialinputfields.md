---
UID: NF:eapmethodpeerapis.EapPeerQueryCredentialInputFields
title: EapPeerQueryCredentialInputFields function (eapmethodpeerapis.h)
description: Defines the implementation of an EAP method-specific function that obtains the EAP Single-Sign-On (SSO) credential input fields for an EAP method.
helpviewer_keywords: ["EapPeerQueryCredentialInputFields","EapPeerQueryCredentialInputFields function [EAPHost]","eaphost.eappeerquerycredentialinputfields","eapmethodpeerapis/EapPeerQueryCredentialInputFields"]
old-location: eaphost\eappeerquerycredentialinputfields.htm
tech.root: eaphost
ms.assetid: 8ae42352-e972-4094-bf03-90a2f20ab641
ms.date: 12/05/2018
ms.keywords: EapPeerQueryCredentialInputFields, EapPeerQueryCredentialInputFields function [EAPHost], eaphost.eappeerquerycredentialinputfields, eapmethodpeerapis/EapPeerQueryCredentialInputFields
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerQueryCredentialInputFields
 - eapmethodpeerapis/EapPeerQueryCredentialInputFields
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerQueryCredentialInputFields
---

# EapPeerQueryCredentialInputFields function


## -description

Defines the implementation of an EAP method-specific function that obtains the EAP  Single-Sign-On (SSO) credential input fields for an EAP method.

## -parameters

### -param hUserImpersonationToken [in]

An impersonation token for the user whose credentials are to be requested and obtained.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwEapConnDataSize [in]

The size of the EAP SSO configuration byte data pointed to by <i>pbEapConnData</i>, in bytes.

### -param pbEapConnData [in]

A Pointer to an opaque byte buffer that contains the EAP configuration data BLOB.

### -param pEapConfigFieldsArray [out]

A Pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the input fields to display to the supplicant user. The <b>pwszData</b> fields in the individual <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data">EAP_CONFIG_INPUT_FIELD_DATA</a> elements are initialized to <b>NULL</b>.

### -param ppEapError [out]

 A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

<b>EapPeerQueryCredentialInputFields</b> supports SSO. This peer method function, like <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields">EapPeerQueryUserBlobFromCredentialInputFields</a>, is used only in an SSO scenario.

 The EAP method-specific implementation of this function is called by EAPHost whenever a supplicant application calls <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields">EapHostPeerQueryCredentialInputFields</a>. The implementer of this function is responsible for ensuring that the  <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> returned by this function contains input field definitions for each piece of credential data the EAP methods will request from the supplicant user.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)