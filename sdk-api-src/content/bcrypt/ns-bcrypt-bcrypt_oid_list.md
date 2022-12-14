---
UID: NS:bcrypt._BCRYPT_OID_LIST
title: BCRYPT_OID_LIST (bcrypt.h)
description: Used to contain a collection of BCRYPT_OID structures. Use this structure with the BCRYPT_HASH_OID_LIST property to retrieve the list of hashing object identifiers (OIDs) that have been encoded by using Distinguished Encoding Rules (DER) encoding.
helpviewer_keywords: ["BCRYPT_OID_LIST","BCRYPT_OID_LIST structure [Security]","bcrypt/BCRYPT_OID_LIST","security.bcrypt_oid_list"]
old-location: security\bcrypt_oid_list.htm
tech.root: security
ms.assetid: 5e07d4a9-88eb-4644-a9be-e39c52b97ea7
ms.date: 12/05/2018
ms.keywords: BCRYPT_OID_LIST, BCRYPT_OID_LIST structure [Security], bcrypt/BCRYPT_OID_LIST, security.bcrypt_oid_list
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: BCRYPT_OID_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_OID_LIST
 - bcrypt/_BCRYPT_OID_LIST
 - BCRYPT_OID_LIST
 - bcrypt/BCRYPT_OID_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_OID_LIST
---

# BCRYPT_OID_LIST structure


## -description

The <b>BCRYPT_OID_LIST</b> structure is used to contain a collection of <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_oid">BCRYPT_OID</a> structures. Use this structure with the <a href="/windows/desktop/SecCNG/cng-property-identifiers">BCRYPT_HASH_OID_LIST</a> property to retrieve the list of hashing <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) that have been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoding.

## -struct-fields

### -field dwOIDCount

The number of elements in the <b>pOIDs</b> array.

### -field pOIDs

The address of an array of <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_oid">BCRYPT_OID</a> structures that contains OIDs.

## -remarks

The first OID in the <b>pOIDs</b> array is used to identify any hashes or signatures created by this algorithm provider. When verifying a hash or signature, all the OIDs in the array are treated as valid.

In the Microsoft Primitive Provider implementation, <b>dwOIDCount</b> is 2, so that the <b>pOIDs</b> array contains two members:

<ul>
<li><b>pOIDs[0]</b> contains a DER-encoded <b>AlgorithmIdentifier</b> with a <b>NULL</b> parameter.</li>
<li><b>pOIDs[1]</b> contains the DER-encoded <b>AlgorithmIdentifier</b> without a <b>NULL</b> parameter.</li>
</ul>
For example, the SHA-1 encoding would be:

<ul>
<li><b>pOIDs[0]</b> --&gt; 06 05 2b 0e 03 02 1a 05 00

</li>
<li><b>pOIDs[1]</b> --&gt; 06 05 2b 0e 03 02 1a</li>
</ul>


The following snippet describes an <b>AlgorithmIdentifier</b> in <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) notation.  <b>SEQUENCE</b>, <b>OBJECT IDENTIFIER</b>, and <b>ANY</b> are DER encoded. The <b>ANY</b> BLOB is <b>NULL</b>.


``` syntax
AlgorithmIdentifier ::= SEQUENCE {
   algorithm            OBJECT IDENTIFIER,
   algorithmParams      ANY
}

```


## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_oid">BCRYPT_OID</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a>



<a href="/windows/desktop/SecCNG/cng-property-identifiers">Cryptography Primitive Property Identifiers</a>
