---
UID: NF:wincrypt.CryptCreateKeyIdentifierFromCSP
title: CryptCreateKeyIdentifierFromCSP function
author: windows-sdk-content
description: Important  This API is deprecated.
old-location: security\cryptcreatekeyidentifierfromcsp.htm
tech.root: seccrypto
ms.assetid: 628e1995-8207-4daa-a445-cb21a755ffa6
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CryptCreateKeyIdentifierFromCSP, CryptCreateKeyIdentifierFromCSP function [Security], _crypto2_cryptcreatekeyidentifierfromcsp, security.cryptcreatekeyidentifierfromcsp, wincrypt/CryptCreateKeyIdentifierFromCSP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
---

# CryptCreateKeyIdentifierFromCSP function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptCreateKeyIdentifierFromCSP</b> function creates a key identifier from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>.

This function converts a <a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a> of a CSP 
into an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a>
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure and encodes it. The encoded structure is then <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashed</a> with the SHA1 algorithm to obtain the key identifier.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pszPubKeyOID [in]

A pointer to the public key <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). A value that is not <b>NULL</b> overrides the default OID obtained from the <b>aiKeyAlg</b> member of the structure pointed to by <i>pPubKeyStruc</i>. To use the default OID, set <i>pszPubKeyOID</i> to <b>NULL</b>.


### -param pPubKeyStruc [in]

A pointer to a 
<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a> structure. In the default case, the <b>aiKeyAlg</b> member of the structure pointed to by <i>pPubKeyStruc</i> is used to find the public key OID. When the value of <i>pszPubKeyOID</i> is not <b>NULL</b>, it overrides the default.


### -param cbPubKeyStruc [in]

The size, in bytes, of the <a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a>.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.


### -param pbHash [out]

A pointer to a buffer to receive the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the public key and the key identifier.

To get the size of this information for memory allocation purposes, set this parameter to <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbHash [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbHash</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. Using SHA1 hashing, the length of the required buffer is twenty.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).
For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/6e57d935-4cfb-44af-b1c6-6c399c959452">CryptEnumKeyIdentifierProperties</a>



<a href="https://msdn.microsoft.com/bc0511c1-0699-4959-afd7-a838c91c77d5">CryptGetKeyIdentifierProperty</a>



<a href="https://msdn.microsoft.com/0970aaaa-3f9a-4471-bd21-5de8746f94a2">CryptSetKeyIdentifierProperty</a>



<a href="cryptography_functions.htm">Key Identifier Functions</a>
 

 

