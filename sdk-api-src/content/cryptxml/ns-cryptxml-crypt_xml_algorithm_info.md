---
UID: NS:cryptxml._CRYPT_XML_ALGORITHM_INFO
title: CRYPT_XML_ALGORITHM_INFO (cryptxml.h)
description: Contains algorithm information.
helpviewer_keywords: ["*PCRYPT_XML_ALGORITHM_INFO","CRYPT_XML_ALGORITHM_INFO","CRYPT_XML_ALGORITHM_INFO structure [Security]","CRYPT_XML_GROUP_ID_HASH","CRYPT_XML_GROUP_ID_SIGN","PCRYPT_XML_ALGORITHM_INFO","PCRYPT_XML_ALGORITHM_INFO structure pointer [Security]","cryptxml/CRYPT_XML_ALGORITHM_INFO","cryptxml/PCRYPT_XML_ALGORITHM_INFO","security.crypt_xml_algorithm_info"]
old-location: security\crypt_xml_algorithm_info.htm
tech.root: security
ms.assetid: ab6ec092-d25d-4ca0-8206-b7e5ad36d69b
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_ALGORITHM_INFO, CRYPT_XML_ALGORITHM_INFO, CRYPT_XML_ALGORITHM_INFO structure [Security], CRYPT_XML_GROUP_ID_HASH, CRYPT_XML_GROUP_ID_SIGN, PCRYPT_XML_ALGORITHM_INFO, PCRYPT_XML_ALGORITHM_INFO structure pointer [Security], cryptxml/CRYPT_XML_ALGORITHM_INFO, cryptxml/PCRYPT_XML_ALGORITHM_INFO, security.crypt_xml_algorithm_info'
req.header: cryptxml.h
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
req.typenames: CRYPT_XML_ALGORITHM_INFO, *PCRYPT_XML_ALGORITHM_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_ALGORITHM_INFO
 - cryptxml/_CRYPT_XML_ALGORITHM_INFO
 - PCRYPT_XML_ALGORITHM_INFO
 - cryptxml/PCRYPT_XML_ALGORITHM_INFO
 - CRYPT_XML_ALGORITHM_INFO
 - cryptxml/CRYPT_XML_ALGORITHM_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_ALGORITHM_INFO
---

# CRYPT_XML_ALGORITHM_INFO structure


## -description

The <b>CRYPT_XML_ALGORITHM_INFO</b> structure contains algorithm information.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field wszAlgorithmURI

A pointer to a null-terminated Unicode string that contains the URI associated with the attribute of the <b>SignatureMethod</b> or <b>DigestMethod</b> element of the XML signature.

### -field wszName

Optional. A pointer to a null-terminated Unicode string that contains the display name of the algorithm.

### -field dwGroupId

A <b>DWORD</b> value that specifies the group type to which the algorithm belongs. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_GROUP_ID_HASH_________"></a><a id="crypt_xml_group_id_hash_________"></a><dl>
<dt><b>CRYPT_XML_GROUP_ID_HASH         </b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Hash algorithms

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_GROUP_ID_SIGN_________"></a><a id="crypt_xml_group_id_sign_________"></a><dl>
<dt><b>CRYPT_XML_GROUP_ID_SIGN         </b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Signature algorithms

</td>
</tr>
</table>

### -field wszCNGAlgid

A pointer to a null-terminated Unicode string that contains an algorithm identifier string that is passed to  Cryptography API: Next Generation (CNG) functions. CNG functions use algorithm identifier strings, such as L"SHA1", instead of the <b>ALG_ID</b> data type constants, such as CALG_SHA1.


<div class="alert"><b>Note</b>  BCrypt* and NCrypt* functions are defined in Bcrypt.h and Ncrypt.h.</div>
<div> </div>

### -field wszCNGExtraAlgid

A pointer to a null-terminated Unicode string that contains an extra algorithm string, other than the string in the <b>pwszCNGAlgid</b> member, that is passed to CNG functions.


<div class="alert"><b>Note</b>  BCrypt* and NCrypt* functions are defined in Bcrypt.h and Ncrypt.h.</div>
<div> </div>

### -field dwSignFlags

A <b>DWORD</b> value that contains flag values to be  passed to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a> function.

### -field dwVerifyFlags

A <b>DWORD</b> value that is passed to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptverifysignature">BCryptVerifySignature</a> function.

### -field pvPaddingInfo

A pointer to a structure that contains padding information to be passed to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a> or <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptverifysignature">BCryptVerifySignature</a> function. The actual type of structure this member points to depends on the value of the <b>dwGroupId</b> member.

### -field pvExtraInfo

Optional. A pointer to a structure that contains extra information that can be passed to the CNG functions.


<div class="alert"><b>Note</b>  BCrypt* and NCrypt* functions are defined in Bcrypt.h and Ncrypt.h.</div>
<div> </div>

## -see-also

<b></b>



<a href="/windows/desktop/SecCrypto/xml-digital-signature-cryptographic-algorithms">Digital Signature Cryptographic Algorithms</a>