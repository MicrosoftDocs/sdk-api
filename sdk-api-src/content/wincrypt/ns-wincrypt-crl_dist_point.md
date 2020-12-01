---
UID: NS:wincrypt._CRL_DIST_POINT
title: CRL_DIST_POINT (wincrypt.h)
description: Identifies a single certificate revocation list (CRL) distribution point that a certificate user can reference to determine whether certificates have been revoked.
helpviewer_keywords: ["*PCRL_DIST_POINT","CRL_DIST_POINT","CRL_DIST_POINT structure [Security]","PCRL_DIST_POINT","PCRL_DIST_POINT structure pointer [Security]","_crypto2_crl_dist_point","security.crl_dist_point","wincrypt/CRL_DIST_POINT","wincrypt/PCRL_DIST_POINT"]
old-location: security\crl_dist_point.htm
tech.root: security
ms.assetid: ec7ccc54-0aaa-4c32-8aa1-dcbaf59f9991
ms.date: 12/05/2018
ms.keywords: '*PCRL_DIST_POINT, CRL_DIST_POINT, CRL_DIST_POINT structure [Security], PCRL_DIST_POINT, PCRL_DIST_POINT structure pointer [Security], _crypto2_crl_dist_point, security.crl_dist_point, wincrypt/CRL_DIST_POINT, wincrypt/PCRL_DIST_POINT'
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
req.typenames: CRL_DIST_POINT, *PCRL_DIST_POINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_DIST_POINT
 - wincrypt/_CRL_DIST_POINT
 - PCRL_DIST_POINT
 - wincrypt/PCRL_DIST_POINT
 - CRL_DIST_POINT
 - wincrypt/CRL_DIST_POINT
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
 - CRL_DIST_POINT
---

# CRL_DIST_POINT structure


## -description

The <b>CRL_DIST_POINT</b> structure identifies a single <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution point that a certificate user can reference to determine whether certificates have been revoked. A certificate user can obtain a CRL from an applicable distribution point or can obtain a current complete CRL from the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) directory entry.

The <b>CRL_DIST_POINT</b> structures are the elements in the array member of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_points_info">CRL_DIST_POINTS_INFO</a> structure.

## -struct-fields

### -field DistPointName

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_point_name">CRL_DIST_POINT_NAME</a> structure that identifies the location of a CRL source. If <b>NULL</b>, the distribution point name defaults to the <b>CRLIssuer</b> name.

### -field ReasonFlags

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a> that contains a byte that indicates the revocation reasons covered by the CRL. 




If <b>NULL</b>, the indicated CRL distribution point distributes a CRL that will contain an entry for this certificate if this certificate has been revoked, regardless of the revocation reason.

The following are currently defined <b>ReasonFlags</b> values. For revocations of several reasons, combine these <b>ReasonFlags</b> by using a bitwise-<b>OR</b> operation.


<ul>
<li>CRL_REASON_UNUSED_FLAG</li>
<li>CRL_REASON_KEY_COMPROMISE_FLAG</li>
<li>CRL_REASON_CA_COMPROMISE_FLAG</li>
<li>CRL_REASON_AFFILIATION_CHANGED_FLAG</li>
<li>CRL_REASON_SUPERSEDED_FLAG</li>
<li>CRL_REASON_CESSATION_OF_OPERATION_FLAG</li>
<li>CRL_REASON_CERTIFICATE_HOLD_FLAG</li>
</ul>

### -field CRLIssuer

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> that identifies the authority that issued and signed the CRL. If <b>NULL</b>, the issuer name defaults to the issuer name of the certificate.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_points_info">CRL_DIST_POINTS_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_dist_point_name">CRL_DIST_POINT_NAME</a>