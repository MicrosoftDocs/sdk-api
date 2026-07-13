---
UID: NF:eapmethodpeerapis.EapPeerQueryUIBlobFromInteractiveUIInputFields
title: EapPeerQueryUIBlobFromInteractiveUIInputFields function (eapmethodpeerapis.h)
description: Converts user information into a user BLOB that can be consumed by EAPHost run-time functions. (EapPeerQueryUIBlobFromInteractiveUIInputFields)
helpviewer_keywords: ["EapPeerQueryUIBlobFromInteractiveUIInputFields","EapPeerQueryUIBlobFromInteractiveUIInputFields function [EAPHost]","eaphost.eappeerqueryuiblobfrominteractiveuiinputfields","eapmethodpeerapis/EapPeerQueryUIBlobFromInteractiveUIInputFields"]
old-location: eaphost\eappeerqueryuiblobfrominteractiveuiinputfields.htm
tech.root: eaphost
ms.assetid: bfb8906e-7adb-4c69-bd13-7c5239d392af
ms.date: 12/05/2018
ms.keywords: EapPeerQueryUIBlobFromInteractiveUIInputFields, EapPeerQueryUIBlobFromInteractiveUIInputFields function [EAPHost], eaphost.eappeerqueryuiblobfrominteractiveuiinputfields, eapmethodpeerapis/EapPeerQueryUIBlobFromInteractiveUIInputFields
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
 - EapPeerQueryUIBlobFromInteractiveUIInputFields
 - eapmethodpeerapis/EapPeerQueryUIBlobFromInteractiveUIInputFields
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
 - EapPeerQueryUIBlobFromInteractiveUIInputFields
---

# EapPeerQueryUIBlobFromInteractiveUIInputFields function


## -description

The <b>EapPeerQueryUIBlobFromInteractiveUIInputFields</b> function converts user information into a user BLOB that can be consumed by EAPHost run-time functions.

## -parameters

### -param dwVersion [in]

The version number of the API. Must be set to zero.

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwSizeofUIContextData [in]

The size of the context data in the <i>pUIContextData</i> parameter, in bytes.

### -param pUIContextData [in]

A pointer to a BLOB that contains UI context data, represented as inner pointers to field data. The supplicant obtained these inner pointers from EAPHost run-time functions.

### -param pEapInteractiveUIData [in]

Pointer that receives an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a> structure that contains configuration information for interactive user interface components raised on an EAP supplicant.

### -param pdwSizeOfDataFromInteractiveUI [out]

A pointer to a DWORD that specifies the size of the buffer pointed to by the <i>ppDataFromInteractiveUI</i> parameter, in bytes. If this value is not set to 0, then a pointer to a buffer of the size specified in this parameter must be supplied in the  <i>ppDataFromInteractiveUI</i> parameter.

### -param ppDataFromInteractiveUI [out]

  A pointer that receives a credentials BLOB that can be used in authentication.
                The caller should free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory">EapPeerFreeMemory</a>, starting at the innermost pointer. If a non-NULL value is supplied for this parameter, meaning that an existing data BLOB is passed to it, the supplied data BLOB will be updated and returned in this parameter.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>.

### -param ppvReserved [in, out]

Reserved for future use. This parameter must be set to 0.

## -remarks

[Peer Method API Call Sequence](/windows/win32/eaphost/peer-method-api-call-sequence).

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)
