---
UID: NF:eapmethodpeerapis.EapPeerQueryUserBlobFromCredentialInputFields
title: EapPeerQueryUserBlobFromCredentialInputFields function (eapmethodpeerapis.h)
description: Defines the implementation of an EAP method function that obtains the user BLOB data provided in an interactive Single-Sign-On (SSO) UI raised on the supplicant.
helpviewer_keywords: ["EapPeerQueryUserBlobFromCredentialInputFields","EapPeerQueryUserBlobFromCredentialInputFields function [EAPHost]","eaphost.eappeerqueryuserblobfrominteractiveuiinputfields","eapmethodpeerapis/EapPeerQueryUserBlobFromCredentialInputFields"]
old-location: eaphost\eappeerqueryuserblobfrominteractiveuiinputfields.htm
tech.root: eaphost
ms.assetid: decfe3cd-642e-41c8-9bec-d079a0f74504
ms.date: 12/05/2018
ms.keywords: EapPeerQueryUserBlobFromCredentialInputFields, EapPeerQueryUserBlobFromCredentialInputFields function [EAPHost], eaphost.eappeerqueryuserblobfrominteractiveuiinputfields, eapmethodpeerapis/EapPeerQueryUserBlobFromCredentialInputFields
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
 - EapPeerQueryUserBlobFromCredentialInputFields
 - eapmethodpeerapis/EapPeerQueryUserBlobFromCredentialInputFields
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
 - EapPeerQueryUserBlobFromCredentialInputFields
---

# EapPeerQueryUserBlobFromCredentialInputFields function


## -description

The <b>EapPeerQueryUserBlobFromCredentialInputFields</b> function defines the implementation of an EAP method function that obtains the user BLOB data provided in an interactive Single-Sign-On (SSO) UI raised on the supplicant.

## -parameters

### -param hUserImpersonationToken [in]

An impersonation token for the user whose credentials are to be requested and obtained.

### -param eapMethodType [in]

An <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that contains vendor and author information about the EAP method used for authenticating the connection.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwEapConnDataSize [in]

The size of the EAP SSO configuration  data pointed to by <i>pbEapConnData</i>, in bytes.

### -param pbEapConnData [in]

A pointer to an opaque byte buffer that contains the EAP SSO configuration data BLOB.

### -param pEapConfigInputFieldArray [in]

A pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure that contains the input fields to display to the supplicant user. The <b>pwszData</b> fields in the individual <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data">EAP_CONFIG_INPUT_FIELD_DATA</a> elements are initialized to <b>NULL</b>.

### -param pdwUserBlobSize [in, out]

A pointer to a buffer that contains the size, in bytes, of the opaque user configuration data BLOB in <i>ppUserBlob</i>.

### -param ppbUserBlob [in, out]

A pointer that contains the opaque user data BLOB.

### -param ppEapError [out]

 A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

## -remarks

<b>EapPeerQueryUserBlobFromCredentialInputFields</b> supports Single-Sign-On (SSO). This peer method function, like <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields">EapPeerQueryCredentialInputFields</a>, is used only in an SSO scenario.

After <b>EapPeerQueryUserBlobFromCredentialInputFields</b>, EAPHost calls <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a>. The supplicant  uses the <b>EAP_FLAG_PRE_LOGON</b> flag in <b>EapHostPeerBeginSession</b> to indicate that EAPHost should provide SSO.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)