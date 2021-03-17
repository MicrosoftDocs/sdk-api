---
UID: NS:wincrypt._EV_EXTRA_CERT_CHAIN_POLICY_STATUS
title: EV_EXTRA_CERT_CHAIN_POLICY_STATUS (wincrypt.h)
description: Contains policy flags returned from a call to the CertVerifyCertificateChainPolicy function.
helpviewer_keywords: ["*PEV_EXTRA_CERT_CHAIN_POLICY_STATUS","CERT_ROOT_PROGRAM_FLAG_LSC","CERT_ROOT_PROGRAM_FLAG_ORG","CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO","EV_EXTRA_CERT_CHAIN_POLICY_STATUS","EV_EXTRA_CERT_CHAIN_POLICY_STATUS structure [Security]","PEV_EXTRA_CERT_CHAIN_POLICY_STATUS","PEV_EXTRA_CERT_CHAIN_POLICY_STATUS structure pointer [Security]","security.ev_extra_cert_chain_policy_status","wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_STATUS","wincrypt/_EV_EXTRA_CERT_CHAIN_POLICY_STATUS"]
old-location: security\ev_extra_cert_chain_policy_status.htm
tech.root: security
ms.assetid: 65810a26-2675-4a98-b2ee-59d4e3bc1994
ms.date: 12/05/2018
ms.keywords: '*PEV_EXTRA_CERT_CHAIN_POLICY_STATUS, CERT_ROOT_PROGRAM_FLAG_LSC, CERT_ROOT_PROGRAM_FLAG_ORG, CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO, EV_EXTRA_CERT_CHAIN_POLICY_STATUS, EV_EXTRA_CERT_CHAIN_POLICY_STATUS structure [Security], PEV_EXTRA_CERT_CHAIN_POLICY_STATUS, PEV_EXTRA_CERT_CHAIN_POLICY_STATUS structure pointer [Security], security.ev_extra_cert_chain_policy_status, wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_STATUS, wincrypt/_EV_EXTRA_CERT_CHAIN_POLICY_STATUS'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: EV_EXTRA_CERT_CHAIN_POLICY_STATUS, *PEV_EXTRA_CERT_CHAIN_POLICY_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EV_EXTRA_CERT_CHAIN_POLICY_STATUS
 - wincrypt/_EV_EXTRA_CERT_CHAIN_POLICY_STATUS
 - PEV_EXTRA_CERT_CHAIN_POLICY_STATUS
 - wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_STATUS
 - EV_EXTRA_CERT_CHAIN_POLICY_STATUS
 - wincrypt/EV_EXTRA_CERT_CHAIN_POLICY_STATUS
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
 - EV_EXTRA_CERT_CHAIN_POLICY_STATUS
---

# EV_EXTRA_CERT_CHAIN_POLICY_STATUS structure


## -description

The <b>EV_EXTRA_CERT_CHAIN_POLICY_STATUS</b> structure is returned in the <b>pvExtraPolicyStatus</b>  member of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_status">CERT_CHAIN_POLICY_STATUS</a> structure. The structure contains policy flags returned from a call to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> function.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwQualifiers

### -field dwIssuanceUsageIndex

A <b>DWORD</b> value that specifies an index in the array of the resultant set of policy OIDs for the chain. The index corresponds to the EV policy OID for which the chain is valid. The policy OID is retrieved by using  
the index, as shown in the following pseudocode:

<code>pChainContext-&gt;rgpChain[0]-&gt;rgpElement[0]-&gt;pIssuanceUsage-&gt;rgpszUsageIdentifier[dwIssuanceUsageIndex];</code>


#### - fQualifiers

A <b>DWORD</b> value that specifies which of the EV policy qualifiers are set corresponding to the policy <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for which the chain is valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_ROOT_PROGRAM_FLAG_ORG"></a><a id="cert_root_program_flag_org"></a><dl>
<dt><b>CERT_ROOT_PROGRAM_FLAG_ORG</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
Validation of the Organization (O) field in the subject name meets Root Program Requirements for display.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ROOT_PROGRAM_FLAG_LSC"></a><a id="cert_root_program_flag_lsc"></a><dl>
<dt><b>CERT_ROOT_PROGRAM_FLAG_LSC</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Validation of the Locale (L), State (S), and Country (C) fields in
the subject name meets Program Requirements for display.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO"></a><a id="cert_root_program_flag_subject_logo"></a><dl>
<dt><b>CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
Validation of the  Subject logotype meets Program Requirements for display.

</td>
</tr>
</table>