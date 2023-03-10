---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryUIBlobFromInteractiveUIInputFields
title: EapHostPeerQueryUIBlobFromInteractiveUIInputFields function (eaphostpeerconfigapis.h)
description: Converts user information into a user BLOB that can be consumed by EAPHost run-time functions. (EapHostPeerQueryUIBlobFromInteractiveUIInputFields)
helpviewer_keywords: ["EAPHOST_PEER_API_VERSION","EapHostPeerQueryUIBlobFromInteractiveUIInputFields","EapHostPeerQueryUIBlobFromInteractiveUIInputFields function [EAPHost]","eaphost.eaphostpeerqueryuiblobfrominteractiveuiinputfields","eaphostpeerconfigapis/EapHostPeerQueryUIBlobFromInteractiveUIInputFields"]
old-location: eaphost\eaphostpeerqueryuiblobfrominteractiveuiinputfields.htm
tech.root: eaphost
ms.assetid: 2c4b1a0b-8c3f-47c5-8829-2f9c9bfda946
ms.date: 12/05/2018
ms.keywords: EAPHOST_PEER_API_VERSION, EapHostPeerQueryUIBlobFromInteractiveUIInputFields, EapHostPeerQueryUIBlobFromInteractiveUIInputFields function [EAPHost], eaphost.eaphostpeerqueryuiblobfrominteractiveuiinputfields, eaphostpeerconfigapis/EapHostPeerQueryUIBlobFromInteractiveUIInputFields
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
 - EapHostPeerQueryUIBlobFromInteractiveUIInputFields
 - eaphostpeerconfigapis/EapHostPeerQueryUIBlobFromInteractiveUIInputFields
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
 - EapHostPeerQueryUIBlobFromInteractiveUIInputFields
---

# EapHostPeerQueryUIBlobFromInteractiveUIInputFields function


## -description

The <b>EapHostPeerQueryUIBlobFromInteractiveUIInputFields</b> function converts user information into a user BLOB that can be consumed by EAPHost run-time functions.

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
The version of the EAPHost Peer APIs.

</td>
</tr>
</table>

### -param dwFlags [in]

A combination of [EAP flags](/windows/win32/eaphost/eap-method-flags) that describe the  EAP authentication session behavior.

### -param dwSizeofUIContextData [in]

The size of the context data in <i>pUIContextData</i>, in bytes.

### -param pUIContextData [in]

Pointer to a BLOB that contains UI context data, represented as inner pointers to field data. These inner pointers must be freed by passing them to <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting with the innermost pointer.

### -param pEapInteractiveUIData [in]

Pointer that receives an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a> structure that contains configuration information for interactive UI components raised on an EAP supplicant.

### -param pdwSizeOfDataFromInteractiveUI [in, out]

A pointer to a DWORD that specifies the size, in bytes, of the buffer pointed to by <i>ppDataFromInteractiveUI</i>. If this value is not set to zero, then a pointer to a buffer of the size specified in this parameter must be supplied to <i>ppDataFromInteractiveUI</i>.

### -param ppDataFromInteractiveUI [in, out]

  Pointer that receives a credentials BLOB that can be used in authentication.
                The caller should free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting at the innermost pointer. If a non-null value is supplied for this parameter (meaning that an existing data BLOB is passed to it), the supplied data BLOB will be updated and returned in this parameter. If a non-NULL BLOB value is supplied, the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function should be used.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

### -param ppvReserved [in, out]

Reserved for future use. This parameter must be set to 0.

## -remarks

[Supplicant API Call Sequence](/windows/win32/eaphost/supplicant-api-call-sequence).

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)
