---
UID: NS:wincrypt._EV_EXTRA_CERT_CHAIN_POLICY_STATUS
title: "_EV_EXTRA_CERT_CHAIN_POLICY_STATUS"
author: windows-sdk-content
description: Contains policy flags returned from a call to the CertVerifyCertificateChainPolicy function.
old-location: security\ev_extra_cert_chain_policy_status.htm
old-project: seccrypto
ms.assetid: 65810a26-2675-4a98-b2ee-59d4e3bc1994
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PEV_EXTRA_CERT_CHAIN_POLICY_STATUS, CERT_ROOT_PROGRAM_FLAG_LSC, CERT_ROOT_PROGRAM_FLAG_ORG, CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO, EV_EXTRA_CERT_CHAIN_POLICY_STATUS, EV_EXTRA_CERT_CHAIN_POLICY_STATUS structure [Security], PEV_EXTRA_CERT_CHAIN_POLICY_STATUS, PEV_EXTRA_CERT_CHAIN_POLICY_STATUS structure pointer [Security], _EV_EXTRA_CERT_CHAIN_POLICY_STATUS, security.ev_extra_cert_chain_policy_status, wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_STATUS, wincrypt/_EV_EXTRA_CERT_CHAIN_POLICY_STATUS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: EV_EXTRA_CERT_CHAIN_POLICY_STATUS, *PEV_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - EV_EXTRA_CERT_CHAIN_POLICY_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _EV_EXTRA_CERT_CHAIN_POLICY_STATUS structure


## -description


The <b>EV_EXTRA_CERT_CHAIN_POLICY_STATUS</b> structure is returned in the <b>pvExtraPolicyStatus</b>  member of a <a href="https://msdn.microsoft.com/599a09b6-fe9e-4489-99ae-8a88fa78a660">CERT_CHAIN_POLICY_STATUS</a> structure. The structure contains policy flags returned from a call to the <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> function.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field dwQualifiers

 


### -field dwIssuanceUsageIndex

A <b>DWORD</b> value that specifies an index in the array of the resultant set of policy OIDs for the chain. The index corresponds to the EV policy OID for which the chain is valid. The policy OID is retrieved by using  
the index, as shown in the following pseudocode:

<code>pChainContext-&gt;rgpChain[0]-&gt;rgpElement[0]-&gt;pIssuanceUsage-&gt;rgpszUsageIdentifier[dwIssuanceUsageIndex];</code>


#### - fQualifiers

A <b>DWORD</b> value that specifies which of the EV policy qualifiers are set corresponding to the policy <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for which the chain is valid.

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
 

