---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryCredentialInputFields
title: EapHostPeerQueryCredentialInputFields function (eaphostpeerconfigapis.h)
description: Allows the user to determine what kind of credentials are required by the methods to perform authentication in a Single-Sign-On (SSO) scenario.
helpviewer_keywords: ["EapHostPeerQueryCredentialInputFields","EapHostPeerQueryCredentialInputFields function [EAPHost]","eaphost.eaphostpeerquerycredentialinputfields","eaphostpeerconfigapis/EapHostPeerQueryCredentialInputFields"]
old-location: eaphost\eaphostpeerquerycredentialinputfields.htm
tech.root: eaphost
ms.assetid: f71aad69-89f3-463b-afd7-9873d582d03b
ms.date: 12/05/2018
ms.keywords: EapHostPeerQueryCredentialInputFields, EapHostPeerQueryCredentialInputFields function [EAPHost], eaphost.eaphostpeerquerycredentialinputfields, eaphostpeerconfigapis/EapHostPeerQueryCredentialInputFields
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerQueryCredentialInputFields
 - eaphostpeerconfigapis/EapHostPeerQueryCredentialInputFields
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerQueryCredentialInputFields
---

# EapHostPeerQueryCredentialInputFields function


## -description

Allows the user to determine what kind of credentials are required by the methods  to perform authentication  in a Single-Sign-On (SSO) scenario.

## -parameters

### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that identifies the EAP method the supplicant is to use.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pbEapConnData.</i>

### -param pbEapConnData [in]

Connection data used for the EAP method.

### -param pEapConfigInputFieldArray [out]

A pointer  to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array">EAP_METHOD_INFO_ARRAY</a> structure for installed EAP methods. The caller should free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting at the innermost pointer.

### -param ppEapError [out]

 
A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

## -remarks

<b>EapHostPeerQueryCredentialInputFields</b> supports Single-Sign-On (SSO).  This supplicant function, like <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuserblobfromcredentialinputfields">EapHostPeerQueryUserBlobFromCredentialInputFields</a>, is used only in an SSO scenario.

<b>EapHostPeerQueryCredentialInputFields</b> obtains the fields to be displayed in the UI during the session. The input fields are obtained to display data entered by the user in the SSO UI. The <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure returned contains details on how to display the input fields.

After <b>EapHostPeerQueryCredentialInputFields</b>, EAPHost calls <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields">EapHostPeerQueryUserBlobFromCredentialInputFields</a>.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)