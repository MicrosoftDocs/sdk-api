---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

