---
UID: NS:wincrypt._AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
title: AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA (wincrypt.h)
description: Holds policy information used in the verification of certificate chains for files.
helpviewer_keywords: ["*PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA","AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA","AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security]","PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA","PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security]","WTPF_ALLOWONLYPERTRUST","WTPF_IGNOREEXPIRATION","WTPF_IGNOREREVOCATIONONTS","WTPF_IGNOREREVOKATION","WTPF_OFFLINEOKNBU_COM","WTPF_OFFLINEOKNBU_IND","WTPF_OFFLINEOK_COM","WTPF_OFFLINEOK_IND","WTPF_TESTCANBEVALID","WTPF_TRUSTTEST","WTPF_VERIFY_V1_OFF","_crypto2_authenticode_extra_cert_chain_policy_para","security.authenticode_extra_cert_chain_policy_para","wincrypt/AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA","wincrypt/PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA"]
old-location: security\authenticode_extra_cert_chain_policy_para.htm
tech.root: security
ms.assetid: 591bd4d4-5062-4282-84fc-f7e02e9592e7
ms.date: 12/05/2018
ms.keywords: '*PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA, AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA, AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security], PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA, PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security], WTPF_ALLOWONLYPERTRUST, WTPF_IGNOREEXPIRATION, WTPF_IGNOREREVOCATIONONTS, WTPF_IGNOREREVOKATION, WTPF_OFFLINEOKNBU_COM, WTPF_OFFLINEOKNBU_IND, WTPF_OFFLINEOK_COM, WTPF_OFFLINEOK_IND, WTPF_TESTCANBEVALID, WTPF_TRUSTTEST, WTPF_VERIFY_V1_OFF, _crypto2_authenticode_extra_cert_chain_policy_para, security.authenticode_extra_cert_chain_policy_para, wincrypt/AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA, wincrypt/PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA, *PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/_AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
 - PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
 - AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA
---

# AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA structure


## -description

The <b>AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_PARA</b> structure holds policy information used in the verification of certificate chains for files.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwRegPolicySettings

Flags set during installation that can be modified by a user. The SetReg tool found in the Authenticode Tool Pack can be used to select or cancel the selection of each value. These flags can be combined using a bitwise-<b>OR</b> operation. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTPF_TRUSTTEST"></a><a id="wtpf_trusttest"></a><dl>
<dt><b>WTPF_TRUSTTEST</b></dt>
</dl>
</td>
<td width="60%">
Trust any "TEST" certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_TESTCANBEVALID"></a><a id="wtpf_testcanbevalid"></a><dl>
<dt><b>WTPF_TESTCANBEVALID</b></dt>
</dl>
</td>
<td width="60%">
Check any "TEST" certificate for validity.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREEXPIRATION"></a><a id="wtpf_ignoreexpiration"></a><dl>
<dt><b>WTPF_IGNOREEXPIRATION</b></dt>
</dl>
</td>
<td width="60%">
Ignore the expiration date on certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREREVOKATION"></a><a id="wtpf_ignorerevokation"></a><dl>
<dt><b>WTPF_IGNOREREVOKATION</b></dt>
</dl>
</td>
<td width="60%">
Ignore revocation checks.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOK_IND"></a><a id="wtpf_offlineok_ind"></a><dl>
<dt><b>WTPF_OFFLINEOK_IND</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any individual certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOK_COM"></a><a id="wtpf_offlineok_com"></a><dl>
<dt><b>WTPF_OFFLINEOK_COM</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any commercial certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOKNBU_IND"></a><a id="wtpf_offlineoknbu_ind"></a><dl>
<dt><b>WTPF_OFFLINEOKNBU_IND</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any individual certificates. Do not use UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_OFFLINEOKNBU_COM"></a><a id="wtpf_offlineoknbu_com"></a><dl>
<dt><b>WTPF_OFFLINEOKNBU_COM</b></dt>
</dl>
</td>
<td width="60%">
If the source is offline, trust any commercial certificates. Do not use checking UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_VERIFY_V1_OFF"></a><a id="wtpf_verify_v1_off"></a><dl>
<dt><b>WTPF_VERIFY_V1_OFF</b></dt>
</dl>
</td>
<td width="60%">
Turn off verification of v1 certificates.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREREVOCATIONONTS"></a><a id="wtpf_ignorerevocationonts"></a><dl>
<dt><b>WTPF_IGNOREREVOCATIONONTS</b></dt>
</dl>
</td>
<td width="60%">
Ignore time stamp revocation checks.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_ALLOWONLYPERTRUST"></a><a id="wtpf_allowonlypertrust"></a><dl>
<dt><b>WTPF_ALLOWONLYPERTRUST</b></dt>
</dl>
</td>
<td width="60%">
Allow only items in personal trust database.

</td>
</tr>
</table>

### -field pSignerInfo

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a> structure that contains information on the signer of the file.