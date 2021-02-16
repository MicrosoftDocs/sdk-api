---
UID: NS:wincrypt._AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
title: AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA (wincrypt.h)
description: The AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA structure contains time stamp policy information that can be used in certificate chain verification of files.
helpviewer_keywords: ["*PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA","AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA","AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security]","PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA","PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security]","WTPF_ALLOWONLYPERTRUST","WTPF_IGNOREEXPIRATION","WTPF_IGNOREREVOCATIONONTS","WTPF_IGNOREREVOKATION","WTPF_OFFLINEOKNBU_COM","WTPF_OFFLINEOKNBU_IND","WTPF_OFFLINEOK_COM","WTPF_OFFLINEOK_IND","WTPF_TESTCANBEVALID","WTPF_TRUSTTEST","WTPF_VERIFY_V1_OFF","_crypto2_authenticode_ts_extra_cert_chain_policy_para","security.authenticode_ts_extra_cert_chain_policy_para","wincrypt/AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA","wincrypt/PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA"]
old-location: security\authenticode_ts_extra_cert_chain_policy_para.htm
tech.root: security
ms.assetid: 4c24c924-f466-42d1-a3e0-e86446750040
ms.date: 12/05/2018
ms.keywords: '*PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA, AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA, AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security], PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA, PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security], WTPF_ALLOWONLYPERTRUST, WTPF_IGNOREEXPIRATION, WTPF_IGNOREREVOCATIONONTS, WTPF_IGNOREREVOKATION, WTPF_OFFLINEOKNBU_COM, WTPF_OFFLINEOKNBU_IND, WTPF_OFFLINEOK_COM, WTPF_OFFLINEOK_IND, WTPF_TESTCANBEVALID, WTPF_TRUSTTEST, WTPF_VERIFY_V1_OFF, _crypto2_authenticode_ts_extra_cert_chain_policy_para, security.authenticode_ts_extra_cert_chain_policy_para, wincrypt/AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA, wincrypt/PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA'
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
req.typenames: AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA, *PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/_AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
 - PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/PAUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
 - AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
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
 - AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA
---

# AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA structure


## -description

The <b>AUTHENTICODE_TS_EXTRA_CERT_CHAIN_POLICY_PARA</b> structure contains time stamp policy information that can be used in certificate chain verification of files.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwRegPolicySettings

Flag set during installation that can be modified by a user. The SetReg tool found in the Authenticode Tool Pack can be used to select or cancel the selection of each value. Flag values can be combined using a bitwise-<b>OR</b> operation.

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
Use expiration date.

</td>
</tr>
<tr>
<td width="40%"><a id="WTPF_IGNOREREVOKATION"></a><a id="wtpf_ignorerevokation"></a><dl>
<dt><b>WTPF_IGNOREREVOKATION</b></dt>
</dl>
</td>
<td width="60%">
Do revocation check.

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

### -field fCommercial

BOOL flag. If <b>TRUE</b>, a signer has been verified by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) as meeting certain minimum financial standards.