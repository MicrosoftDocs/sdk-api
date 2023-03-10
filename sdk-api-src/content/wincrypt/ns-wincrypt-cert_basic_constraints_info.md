---
UID: NS:wincrypt._CERT_BASIC_CONSTRAINTS_INFO
title: CERT_BASIC_CONSTRAINTS_INFO (wincrypt.h)
description: The CERT_BASIC_CONSTRAINTS_INFO structure contains information that indicates whether the certified subject can act as a certification authority (CA), an end entity, or both.
helpviewer_keywords: ["*PCERT_BASIC_CONSTRAINTS_INFO","CERT_BASIC_CONSTRAINTS_INFO","CERT_BASIC_CONSTRAINTS_INFO structure [Security]","PCERT_BASIC_CONSTRAINTS_INFO","PCERT_BASIC_CONSTRAINTS_INFO structure pointer [Security]","_crypto2_cert_basic_constraints_info","security.cert_basic_constraints_info","wincrypt/CERT_BASIC_CONSTRAINTS_INFO","wincrypt/PCERT_BASIC_CONSTRAINTS_INFO"]
old-location: security\cert_basic_constraints_info.htm
tech.root: security
ms.assetid: 6603b627-5e5d-48bc-b200-c8dcdd646994
ms.date: 12/05/2018
ms.keywords: '*PCERT_BASIC_CONSTRAINTS_INFO, CERT_BASIC_CONSTRAINTS_INFO, CERT_BASIC_CONSTRAINTS_INFO structure [Security], PCERT_BASIC_CONSTRAINTS_INFO, PCERT_BASIC_CONSTRAINTS_INFO structure pointer [Security], _crypto2_cert_basic_constraints_info, security.cert_basic_constraints_info, wincrypt/CERT_BASIC_CONSTRAINTS_INFO, wincrypt/PCERT_BASIC_CONSTRAINTS_INFO'
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
req.typenames: CERT_BASIC_CONSTRAINTS_INFO, *PCERT_BASIC_CONSTRAINTS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_BASIC_CONSTRAINTS_INFO
 - wincrypt/_CERT_BASIC_CONSTRAINTS_INFO
 - PCERT_BASIC_CONSTRAINTS_INFO
 - wincrypt/PCERT_BASIC_CONSTRAINTS_INFO
 - CERT_BASIC_CONSTRAINTS_INFO
 - wincrypt/CERT_BASIC_CONSTRAINTS_INFO
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
 - CERT_BASIC_CONSTRAINTS_INFO
---

# CERT_BASIC_CONSTRAINTS_INFO structure


## -description

The <b>CERT_BASIC_CONSTRAINTS_INFO</b> structure contains information that indicates whether the certified subject can act as a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA), an end entity, or both. If the subject can act as a CA, a certification path-length constraint can also be specified, as can a set of subtrees that must contain all subject names of subsequent certificates in a certification chain. This extension is used in validating certificates used to sign other certificates.

The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> function creates an instance of this structure when performed on a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member with its structure's <b>pszObjId</b> member set to szOID_BASIC_CONSTRAINTS.

## -struct-fields

### -field SubjectType

A
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a> value can contain one of the following:

<ul>
<li>A CERT_CA_SUBJECT_FLAG that, when set, indicates that the certificate's subject can act as a CA.</li>
<li>A CERT_END_ENTITY_SUBJECT_FLAG that, when set, indicates that the certificate's subject can act as an end entity.</li>
<li>Both of the above, combined using a bitwise-<b>OR</b> operation.</li>
</ul>

### -field fPathLenConstraint

A Boolean value that indicates whether the <b>dwPathLenConstraint</b> field sets the maximum length of the certification path.

### -field dwPathLenConstraint

The maximum number of CA certificates that can follow this certificate in a certification validation path. A value of zero indicates that the subject of this certificate can issue certificates only to end entities and not to CAs.

### -field cSubtreesConstraint

The number of elements in the <b>rgSubtreesConstraint</b> array.

### -field rgSubtreesConstraint

An array of 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structures that establish subtree constraints.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>