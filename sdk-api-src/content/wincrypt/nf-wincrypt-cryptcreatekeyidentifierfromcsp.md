---
UID: NF:wincrypt.CryptCreateKeyIdentifierFromCSP
title: CryptCreateKeyIdentifierFromCSP function (wincrypt.h)
author: windows-sdk-content
description: Important  This API is deprecated.
old-location: security\cryptcreatekeyidentifierfromcsp.htm
tech.root: SecCrypto
ms.assetid: 628e1995-8207-4daa-a445-cb21a755ffa6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptCreateKeyIdentifierFromCSP, CryptCreateKeyIdentifierFromCSP function [Security], _crypto2_cryptcreatekeyidentifierfromcsp, security.cryptcreatekeyidentifierfromcsp, wincrypt/CryptCreateKeyIdentifierFromCSP
ms.topic: function
f1_keywords: ["wincrypt/CryptCreateKeyIdentifierFromCSP"]
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptCreateKeyIdentifierFromCSP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptCreateKeyIdentifierFromCSP function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptCreateKeyIdentifierFromCSP</b> function creates a key identifier from a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a> <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>.

This function converts a <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_publickeystruc">PUBLICKEYSTRUC</a> of a CSP 
into an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/x-gly">X.509</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure and encodes it. The encoded structure is then <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hashed</a> with the SHA1 algorithm to obtain the key identifier.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pszPubKeyOID [in]

A pointer to the public key <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). A value that is not <b>NULL</b> overrides the default OID obtained from the <b>aiKeyAlg</b> member of the structure pointed to by <i>pPubKeyStruc</i>. To use the default OID, set <i>pszPubKeyOID</i> to <b>NULL</b>.


### -param pPubKeyStruc [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_publickeystruc">PUBLICKEYSTRUC</a> structure. In the default case, the <b>aiKeyAlg</b> member of the structure pointed to by <i>pPubKeyStruc</i> is used to find the public key OID. When the value of <i>pszPubKeyOID</i> is not <b>NULL</b>, it overrides the default.


### -param cbPubKeyStruc [in]

The size, in bytes, of the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_publickeystruc">PUBLICKEYSTRUC</a>.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.


### -param pbHash [out]

A pointer to a buffer to receive the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash</a> of the public key and the key identifier.

To get the size of this information for memory allocation purposes, set this parameter to <b>NULL</b>. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.


### -param pcbHash [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbHash</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. Using SHA1 hashing, the length of the required buffer is twenty.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).
For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties">CryptEnumKeyIdentifierProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty">CryptGetKeyIdentifierProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty">CryptSetKeyIdentifierProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Key Identifier Functions</a>
 

 

