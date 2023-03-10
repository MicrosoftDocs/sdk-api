---
UID: NS:bcrypt._CRYPT_INTERFACE_REG
title: CRYPT_INTERFACE_REG (bcrypt.h)
description: Used to contain information about the type of interface supported by a CNG provider.
helpviewer_keywords: ["*PCRYPT_INTERFACE_REG","BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","BCRYPT_CIPHER_INTERFACE","BCRYPT_HASH_INTERFACE","BCRYPT_RNG_INTERFACE","BCRYPT_SECRET_AGREEMENT_INTERFACE","BCRYPT_SIGNATURE_INTERFACE","CRYPT_DOMAIN","CRYPT_INTERFACE_REG","CRYPT_INTERFACE_REG structure [Security]","CRYPT_LOCAL","NCRYPT_KEY_STORAGE_INTERFACE","NCRYPT_SCHANNEL_INTERFACE","PCRYPT_INTERFACE_REG","PCRYPT_INTERFACE_REG structure pointer [Security]","bcrypt/CRYPT_INTERFACE_REG","bcrypt/PCRYPT_INTERFACE_REG","security.crypt_interface_reg"]
old-location: security\crypt_interface_reg.htm
tech.root: security
ms.assetid: 80204d2a-ebc8-40f6-bccb-7cd112d7769b
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_INTERFACE_REG, BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, BCRYPT_CIPHER_INTERFACE, BCRYPT_HASH_INTERFACE, BCRYPT_RNG_INTERFACE, BCRYPT_SECRET_AGREEMENT_INTERFACE, BCRYPT_SIGNATURE_INTERFACE, CRYPT_DOMAIN, CRYPT_INTERFACE_REG, CRYPT_INTERFACE_REG structure [Security], CRYPT_LOCAL, NCRYPT_KEY_STORAGE_INTERFACE, NCRYPT_SCHANNEL_INTERFACE, PCRYPT_INTERFACE_REG, PCRYPT_INTERFACE_REG structure pointer [Security], bcrypt/CRYPT_INTERFACE_REG, bcrypt/PCRYPT_INTERFACE_REG, security.crypt_interface_reg'
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
req.typenames: CRYPT_INTERFACE_REG, *PCRYPT_INTERFACE_REG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_INTERFACE_REG
 - bcrypt/_CRYPT_INTERFACE_REG
 - PCRYPT_INTERFACE_REG
 - bcrypt/PCRYPT_INTERFACE_REG
 - CRYPT_INTERFACE_REG
 - bcrypt/CRYPT_INTERFACE_REG
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
 - CRYPT_INTERFACE_REG
---

# CRYPT_INTERFACE_REG structure


## -description

The <b>CRYPT_INTERFACE_REG</b> structure is used to contain information about the type of interface supported by a CNG provider.

## -struct-fields

### -field dwInterface

Contains the identifier of the interface type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></a><a id="bcrypt_asymmetric_encryption_interface"></a><dl>
<dt><b>BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the asymmetric encryption interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_INTERFACE"></a><a id="bcrypt_cipher_interface"></a><dl>
<dt><b>BCRYPT_CIPHER_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the cipher interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_INTERFACE"></a><a id="bcrypt_hash_interface"></a><dl>
<dt><b>BCRYPT_HASH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the hash interface.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_KEY_STORAGE_INTERFACE"></a><a id="ncrypt_key_storage_interface"></a><dl>
<dt><b>NCRYPT_KEY_STORAGE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the key storage interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_INTERFACE"></a><a id="bcrypt_rng_interface"></a><dl>
<dt><b>BCRYPT_RNG_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the random number generator interface.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SCHANNEL_INTERFACE"></a><a id="ncrypt_schannel_interface"></a><dl>
<dt><b>NCRYPT_SCHANNEL_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the Schannel interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></a><a id="bcrypt_secret_agreement_interface"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the secret agreement interface.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_INTERFACE"></a><a id="bcrypt_signature_interface"></a><dl>
<dt><b>BCRYPT_SIGNATURE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider supports the signature interface.

</td>
</tr>
</table>

### -field dwFlags

Contains flags that modify the behavior of the interface. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DOMAIN"></a><a id="crypt_domain"></a><dl>
<dt><b>CRYPT_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
This value is not available for use.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LOCAL"></a><a id="crypt_local"></a><dl>
<dt><b>CRYPT_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The interface is registered in the local configuration table.

</td>
</tr>
</table>

### -field cFunctions

Contains the number of elements in the <b>rgpszFunctions</b> array.

### -field rgpszFunctions

An array of null-terminated Unicode strings that contains the identifiers of the algorithms that are supported by this interface. These identifiers can be the standard <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifiers for other registered algorithms.

## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_image_reg">CRYPT_IMAGE_REG</a>