---
UID: NS:wincrypt._CRYPT_SMIME_CAPABILITY
title: CRYPT_SMIME_CAPABILITY (wincrypt.h)
description: The CRYPT_SMIME_CAPABILITY structure specifies a single capability and its associated parameters. Single capabilities are grouped together into a list of CRYPT_SMIME_CAPABILITIES which can specify a prioritized list of capability preferences.
helpviewer_keywords: ["*PCRYPT_SMIME_CAPABILITY","CRYPT_SMIME_CAPABILITY","CRYPT_SMIME_CAPABILITY structure [Security]","PCRYPT_SMIME_CAPABILITY","PCRYPT_SMIME_CAPABILITY structure pointer [Security]","_crypto2_crypt_smime_capability","security.crypt_smime_capability","wincrypt/CRYPT_SMIME_CAPABILITY","wincrypt/PCRYPT_SMIME_CAPABILITY"]
old-location: security\crypt_smime_capability.htm
tech.root: security
ms.assetid: c7d1e04f-d2b9-4bab-88f4-8a528c527e7c
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_SMIME_CAPABILITY, CRYPT_SMIME_CAPABILITY, CRYPT_SMIME_CAPABILITY structure [Security], PCRYPT_SMIME_CAPABILITY, PCRYPT_SMIME_CAPABILITY structure pointer [Security], _crypto2_crypt_smime_capability, security.crypt_smime_capability, wincrypt/CRYPT_SMIME_CAPABILITY, wincrypt/PCRYPT_SMIME_CAPABILITY'
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
req.typenames: CRYPT_SMIME_CAPABILITY, *PCRYPT_SMIME_CAPABILITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_SMIME_CAPABILITY
 - wincrypt/_CRYPT_SMIME_CAPABILITY
 - PCRYPT_SMIME_CAPABILITY
 - wincrypt/PCRYPT_SMIME_CAPABILITY
 - CRYPT_SMIME_CAPABILITY
 - wincrypt/CRYPT_SMIME_CAPABILITY
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
 - CRYPT_SMIME_CAPABILITY
---

# CRYPT_SMIME_CAPABILITY structure


## -description

The <b>CRYPT_SMIME_CAPABILITY</b> structure specifies a single capability and its associated parameters. Single capabilities are grouped together into a list of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_smime_capabilities">CRYPT_SMIME_CAPABILITIES</a> which can specify a prioritized list of capability preferences.
<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_smime_capabilities">CRYPT_SMIME_CAPABILITIES</a> is part of an Internet draft proposal. For a complete definition, see "draft-dusse-s/mime-cert-01.txt" dated May 5, 1997.</div><div> </div>

## -struct-fields

### -field pszObjId

<a href="/windows/desktop/SecGloss/o-gly">Object identifier</a> (OID) for a capability. Capabilities include signature algorithms, <a href="/windows/desktop/SecGloss/s-gly">symmetric algorithms</a>, and key enciphering algorithms. Also included are non-algorithm capabilities, which are the preference for <a href="/windows/desktop/SecGloss/s-gly">signed data</a> and the preference for unencrypted messages.

### -field Parameters

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> structure that contains any parameters associated with the specified capability in <b>pszObjId</b>. 




<div class="alert"><b>Note</b>  For 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a> with the <i>dwCertEncodingType</i> set to X509_ASN_ENCODING, if the <b>cbData</b> member of the <b>Parameters</b> member is zero, the encoded parameters are omitted. They are not encoded as a <b>NULL</b> (05 00) as is done when encoding a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>. This follows the <a href="/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) specification for encoding capabilities that requires this omission.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_smime_capabilities">CRYPT_SMIME_CAPABILITIES</a>