---
UID: NF:eapmethodpeerapis.EapPeerQueryInteractiveUIInputFields
title: EapPeerQueryInteractiveUIInputFields function (eapmethodpeerapis.h)
description: Defines the implementation of an EAP method API that provides the input fields for interactive UI components to be raised on the supplicant.
helpviewer_keywords: ["EapPeerQueryInteractiveUIInputFields","EapPeerQueryInteractiveUIInputFields function [EAPHost]","eaphost.eappeerqueryinteractiveuiinputfields","eapmethodpeerapis/EapPeerQueryInteractiveUIInputFields"]
old-location: eaphost\eappeerqueryinteractiveuiinputfields.htm
tech.root: eaphost
ms.assetid: 7019e13f-d5ad-40ba-8e70-8ded4b136d6c
ms.date: 12/05/2018
ms.keywords: EapPeerQueryInteractiveUIInputFields, EapPeerQueryInteractiveUIInputFields function [EAPHost], eaphost.eappeerqueryinteractiveuiinputfields, eapmethodpeerapis/EapPeerQueryInteractiveUIInputFields
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
 - EapPeerQueryInteractiveUIInputFields
 - eapmethodpeerapis/EapPeerQueryInteractiveUIInputFields
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
 - EapPeerQueryInteractiveUIInputFields
---

# EapPeerQueryInteractiveUIInputFields function


## -description

The <b>EapPeerQueryInteractiveUIInputFields</b> function defines the implementation of an EAP method API that provides the input fields for interactive UI components to be raised on the supplicant.

## -parameters

### -param dwVersion [in]

The version number of the API. Must be set to zero.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwSizeofUIContextData [in]

The size of the context data in <i>pUIContextData</i>, in bytes.

### -param pUIContextData [in]

A pointer to a BLOB that contains UI context data, represented as inner pointers to field data. The supplicant obtained these inner pointers from EAPHost run-time APIs.

### -param pEapInteractiveUIData [out]

Pointer that receives an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a> structure that  contains configuration information for interactive UI components raised on an EAP supplicant.

### -param ppEapError [out]

 A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -param ppvReserved [in, out]

Reserved for future usage. Must be set to <b>NULL</b>

## -remarks

[EapPeerQueryInteractiveUIInputFields](/windows/win32/eaphost/understanding-sso-and-plap) can be employed to support Single-Sign-On (SSO). The <b>EAP_FLAG_PRE_LOGON</b> flag in <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession">EapPeerBeginSession</a> indicates to EAPHost that SSO should be provided. If the <b>EapPeerResponseInvokeUI</b> action code is received after calling <b>EapPeerBeginSession</b>, EAPHost then calls <b>EapPeerQueryInteractiveUIInputFields</b>, and later calls <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryuiblobfrominteractiveuiinputfields">EapPeerQueryUIBlobFromInteractiveUIInputFields</a>.

The supplicant should call  always call the [EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED](/windows/win32/eaphost/eap-related-error-and-information-constants) is returned, the supplicant should resort to the traditional model of invoking method interactive UI by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeinteractiveui">EapPeerInvokeInteractiveUI</a>. If there is an error, <b>EapPeerQueryInteractiveUIInputFields</b> will return a return code other than <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)