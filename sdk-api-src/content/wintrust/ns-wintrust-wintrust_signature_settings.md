---
UID: NS:wintrust.WINTRUST_SIGNATURE_SETTINGS_
title: WINTRUST_SIGNATURE_SETTINGS (wintrust.h)
description: Can be used to specify the signatures on a file.
helpviewer_keywords: ["*PWINTRUST_SIGNATURE_SETTINGS","PWINTRUST_SIGNATURE_SETTINGS","PWINTRUST_SIGNATURE_SETTINGS structure pointer [Security]","WINTRUST_SIGNATURE_SETTINGS","WINTRUST_SIGNATURE_SETTINGS structure [Security]","WSS_GET_SECONDARY_SIG_COUNT","WSS_VERIFY_SPECIFIC","security.wintrust_signature_settings","wintrust/PWINTRUST_SIGNATURE_SETTINGS","wintrust/WINTRUST_SIGNATURE_SETTINGS"]
old-location: security\wintrust_signature_settings.htm
tech.root: security
ms.assetid: E0F526B4-AFDE-4481-B49F-EE7467F97A46
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_SIGNATURE_SETTINGS, PWINTRUST_SIGNATURE_SETTINGS, PWINTRUST_SIGNATURE_SETTINGS structure pointer [Security], WINTRUST_SIGNATURE_SETTINGS, WINTRUST_SIGNATURE_SETTINGS structure [Security], WSS_GET_SECONDARY_SIG_COUNT, WSS_VERIFY_SPECIFIC, security.wintrust_signature_settings, wintrust/PWINTRUST_SIGNATURE_SETTINGS, wintrust/WINTRUST_SIGNATURE_SETTINGS'
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WINTRUST_SIGNATURE_SETTINGS, *PWINTRUST_SIGNATURE_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINTRUST_SIGNATURE_SETTINGS_
 - wintrust/WINTRUST_SIGNATURE_SETTINGS_
 - PWINTRUST_SIGNATURE_SETTINGS
 - wintrust/PWINTRUST_SIGNATURE_SETTINGS
 - WINTRUST_SIGNATURE_SETTINGS
 - wintrust/WINTRUST_SIGNATURE_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_SIGNATURE_SETTINGS
---

# WINTRUST_SIGNATURE_SETTINGS structure


## -description

The <b>WINTRUST_SIGNATURE_SETTINGS</b> structure can be used to specify the signatures on a file.

## -struct-fields

### -field cbStruct

Size, in bytes, of this structure.

### -field dwIndex

Contains the index of the signature to be validated if the <b>dwFlags</b> member is set to <b>WSS_VERIFY_SPECIFIC</b>.

### -field dwFlags

Flags that can be used to refine behavior. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSS_VERIFY_SPECIFIC"></a><a id="wss_verify_specific"></a><dl>
<dt><b>WSS_VERIFY_SPECIFIC</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set this value if you set the <b>dwIndex</b> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="WSS_GET_SECONDARY_SIG_COUNT"></a><a id="wss_get_secondary_sig_count"></a><dl>
<dt><b>WSS_GET_SECONDARY_SIG_COUNT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Set this value to return the number of secondary signatures found in the <b>cSecondarySigs</b> member.

</td>
</tr>
</table>

### -field cSecondarySigs

Contains the number of secondary signatures found if the <b>dwFlags</b> member is set to <b>WSS_GET_SECONDARY_SIG_COUNT</b>.

### -field dwVerifiedSigIndex

The index used for verification. This member is set on return from Wintrust.

### -field pCryptoPolicy

Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure that contains the policy that a signature must pass to be considered valid.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a>



<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a>