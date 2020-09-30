---
UID: NS:wincrypt._CERT_USAGE_MATCH
title: CERT_USAGE_MATCH (wincrypt.h)
description: Provides criteria for identifying issuer certificates to be used to build a certificate chain.
helpviewer_keywords: ["*PCERT_USAGE_MATCH","CERT_USAGE_MATCH","CERT_USAGE_MATCH structure [Security]","PCERT_USAGE_MATCH","PCERT_USAGE_MATCH structure pointer [Security]","USAGE_MATCH_TYPE_AND","USAGE_MATCH_TYPE_OR","_crypto2_cert_usage_match","security.cert_usage_match","wincrypt/CERT_USAGE_MATCH","wincrypt/PCERT_USAGE_MATCH"]
old-location: security\cert_usage_match.htm
tech.root: security
ms.assetid: 6154f1f7-4293-4b8e-91ab-9f57bb6f5743
ms.date: 12/05/2018
ms.keywords: '*PCERT_USAGE_MATCH, CERT_USAGE_MATCH, CERT_USAGE_MATCH structure [Security], PCERT_USAGE_MATCH, PCERT_USAGE_MATCH structure pointer [Security], USAGE_MATCH_TYPE_AND, USAGE_MATCH_TYPE_OR, _crypto2_cert_usage_match, security.cert_usage_match, wincrypt/CERT_USAGE_MATCH, wincrypt/PCERT_USAGE_MATCH'
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
req.typenames: CERT_USAGE_MATCH, *PCERT_USAGE_MATCH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_USAGE_MATCH
 - wincrypt/_CERT_USAGE_MATCH
 - PCERT_USAGE_MATCH
 - wincrypt/PCERT_USAGE_MATCH
 - CERT_USAGE_MATCH
 - wincrypt/CERT_USAGE_MATCH
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
 - CERT_USAGE_MATCH
---

# CERT_USAGE_MATCH structure


## -description

The <b>CERT_USAGE_MATCH</b> structure provides criteria for identifying issuer certificates to be used to build a certificate chain.

## -struct-fields

### -field dwType

Determines the kind of issuer matching to be done. In <b>AND</b> logic, the certificate must meet all criteria. In <b>OR</b> logic, the certificate must meet at least one of the criteria. The following codes are defined to determine the logic used in the match. For more information about how this applied, see Remarks.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USAGE_MATCH_TYPE_AND"></a><a id="usage_match_type_and"></a><dl>
<dt><b>USAGE_MATCH_TYPE_AND</b></dt>
</dl>
</td>
<td width="60%">
<b>AND</b> logic

</td>
</tr>
<tr>
<td width="40%"><a id="USAGE_MATCH_TYPE_OR"></a><a id="usage_match_type_or"></a><dl>
<dt><b>USAGE_MATCH_TYPE_OR</b></dt>
</dl>
</td>
<td width="60%">
<b>OR</b> logic

</td>
</tr>
</table>
 

Default usage match logic is USAGE_MATCH_TYPE_AND.

### -field Usage

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure (<b>CERT_ENHKEY_USAGE</b> is an alternate typedef name for the <b>CTL_USAGE</b> structure) that includes an array of certificate <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) that a certificate must match in order to be valid.

## -remarks

If the <i>dwType</i> member is set to <b>USAGE_MATCH_TYPE_OR</b>, the <i>Usage</i> member cannot be empty.

If the <i>dwType</i> member is set to <b>USAGE_MATCH_TYPE_AND</b>, an empty <i>Usage</i> member means that any nested usage in the chain will work.

The following describes the behavior given two enhanced key usage (EKU) extensions EKU A and EKU B.

<h3><a id="AND_Logic"></a><a id="and_logic"></a><a id="AND_LOGIC"></a>AND Logic</h3>
 If the caller specifies EKU A AND EKU B then the target certificate is valid if EKU A and EKU B are supported by every certificate in the path (either by an explicit EKU setting or through an absent EKU extension in CA certificates.)

<h3><a id="OR_Logic"></a><a id="or_logic"></a><a id="OR_LOGIC"></a>OR Logic</h3>
If the caller specifies EKU A OR EKU B then the target certificate is valid if either EKU A or EKU B is supported in the path.

 Besides the simple case where the certificates in the path contain EKU A or EKU B, the <b>OR</b> clause has the following special evaluation.

Given the following path, the <b>OR</b> test is deemed valid:

 Although the intersection of the EKUs in the chain is an empty set, the use of the EE certificate is valid for EKU A because the request to the cryptography API specifies that the certificate is valid if each certificate of the path supports either EKU A OR EKU B.