---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryUserBlobFromCredentialInputFields
title: EapHostPeerQueryUserBlobFromCredentialInputFields function (eaphostpeerconfigapis.h)
description: Obtains a credential BLOB that can be used to start authentication from user input received from the Single-Sign-On (SSO) UI.
helpviewer_keywords: ["EapHostPeerQueryUserBlobFromCredentialInputFields","EapHostPeerQueryUserBlobFromCredentialInputFields function [EAPHost]","eaphost.eaphostpeerqueryuserblobfromcredentialinputfields","eaphostpeerconfigapis/EapHostPeerQueryUserBlobFromCredentialInputFields"]
old-location: eaphost\eaphostpeerqueryuserblobfromcredentialinputfields.htm
tech.root: eaphost
ms.assetid: bd4fafce-7ece-4cdc-9307-4d41538a4f49
ms.date: 12/05/2018
ms.keywords: EapHostPeerQueryUserBlobFromCredentialInputFields, EapHostPeerQueryUserBlobFromCredentialInputFields function [EAPHost], eaphost.eaphostpeerqueryuserblobfromcredentialinputfields, eaphostpeerconfigapis/EapHostPeerQueryUserBlobFromCredentialInputFields
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
 - EapHostPeerQueryUserBlobFromCredentialInputFields
 - eaphostpeerconfigapis/EapHostPeerQueryUserBlobFromCredentialInputFields
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
 - EapHostPeerQueryUserBlobFromCredentialInputFields
---

# EapHostPeerQueryUserBlobFromCredentialInputFields function


## -description

The <b>EapHostPeerQueryUserBlobFromCredentialInputFields</b> function obtains
a credential BLOB that can be used to start authentication from user input received from the Single-Sign-On (SSO) UI.

## -parameters

### -param hUserImpersonationToken [in]

A handle to the user impersonation token to use in this session.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that specifies the type of EAP authentication to use for this session.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwEapConnDataSize [in]

The size, in bytes, of the connection data buffer provided in <i>pConnectionData.</i>

### -param pbEapConnData [in]

Connection data used for the EAP method.

### -param pEapConfigInputFieldArray [in]

A pointer  to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure the contains the UI input field data. The caller should free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting at the innermost pointer.

### -param pdwUserBlobSize [in, out]

A pointer to a DWORD that specifies the size, in bytes, of the buffer pointed to by <i>ppbUserBlob</i>. If this value is not set to zero, then a pointer to a buffer of the size specified in this parameter must be supplied to <i>ppbUserBlob</i>.

### -param ppbUserBlob [in, out]

A pointer to the credential BLOB that can be used in authentication.
                Memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>. If a non-null value is supplied for this parameter (meaning that an existing data BLOB is passed to it), the supplied data BLOB will be updated and returned in this parameter.  If a non-NULL BLOB value is supplied, the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function should be used.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

## -remarks

<b>EapHostPeerQueryUserBlobFromCredentialInputFields</b> supports SSO. This supplicant function, like <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields">EapHostPeerQueryCredentialInputFields</a>, is used only in an SSO scenario.

After <b>EapHostPeerQueryUserBlobFromCredentialInputFields</b>, EAPHost calls <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>. The supplicant  uses the <b>EAP_FLAG_PRE_LOGON</b> flag in <b>EapHostPeerBeginSession</b> to indicate that EAPHost should provide SSO.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)