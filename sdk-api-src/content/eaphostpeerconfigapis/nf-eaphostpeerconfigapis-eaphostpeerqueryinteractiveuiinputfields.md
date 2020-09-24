---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryInteractiveUIInputFields
title: EapHostPeerQueryInteractiveUIInputFields function (eaphostpeerconfigapis.h)
description: Obtains the input fields for interactive UI components to be raised on the supplicant.
helpviewer_keywords: ["EAPHOST_PEER_API_VERSION","EapHostPeerQueryInteractiveUIInputFields","EapHostPeerQueryInteractiveUIInputFields function [EAPHost]","eaphost.eaphostpeerqueryinteractiveuiinputfields","eaphostpeerconfigapis/EapHostPeerQueryInteractiveUIInputFields"]
old-location: eaphost\eaphostpeerqueryinteractiveuiinputfields.htm
tech.root: eaphost
ms.assetid: facf4ccf-c2e3-435e-8333-8d2c5bbe0186
ms.date: 12/05/2018
ms.keywords: EAPHOST_PEER_API_VERSION, EapHostPeerQueryInteractiveUIInputFields, EapHostPeerQueryInteractiveUIInputFields function [EAPHost], eaphost.eaphostpeerqueryinteractiveuiinputfields, eaphostpeerconfigapis/EapHostPeerQueryInteractiveUIInputFields
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
 - EapHostPeerQueryInteractiveUIInputFields
 - eaphostpeerconfigapis/EapHostPeerQueryInteractiveUIInputFields
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
 - EapHostPeerQueryInteractiveUIInputFields
---

# EapHostPeerQueryInteractiveUIInputFields function


## -description

The <b>EapHostPeerQueryInteractiveUIInputFields</b> function obtains the input fields for interactive UI components to be raised on the supplicant.

## -parameters

### -param dwVersion [in]

The version number of the API. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAPHOST_PEER_API_VERSION"></a><a id="eaphost_peer_api_version"></a><dl>
<dt><b>EAPHOST_PEER_API_VERSION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The version of the EAPHost peer API.

</td>
</tr>
</table>

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwSizeofUIContextData [in]

The size of the context data in <i>pUIContextData</i>, in bytes.

### -param pUIContextData [in]

Pointer to a BLOB that contains UI context data, represented as inner pointers to field data. These inner pointers must be freed by passing them to <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting with the innermost pointer.

### -param pEapInteractiveUIData [out]

Pointer that receives an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a> structure that contains configuration information for interactive UI components raised on an EAP supplicant. The caller should free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting at the innermost pointer.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

### -param ppvReserved [in, out]

Reserved for future use. This parameter must be set to 0.

## -remarks

<b>EapHostPeerQueryInteractiveUIInputFields</b> can be employed to support Single-Sign-On (SSO). The supplicant  uses the <b>EAP_FLAG_PRE_LOGON</b> flag in <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a> to indicate to EAPHost that SSO should be provided. If the <a href="/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseInvokeUI</a> action code is received after calling <b>EapHostPeerBeginSession</b>, EAPHost then calls <b>EapHostPeerQueryInteractiveUIInputFields</b>, and later calls <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields">EapHostPeerQueryUIBlobFromInteractiveUIInputFields</a>. 

The supplicant should call the [EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED](/windows/win32/eaphost/eap-related-error-and-information-constants) is returned, the supplicant should resort to the traditional model of invoking method interactive UI by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui">EapHostPeerInvokeInteractiveUI</a>. If there is an error, <b>EapHostPeerQueryInteractiveUIInputFields</b> will return a return code other than <b>NULL</b>.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)