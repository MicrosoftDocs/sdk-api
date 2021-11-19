---
UID: NF:wincrypt.CryptGetMessageSignerCount
title: CryptGetMessageSignerCount function (wincrypt.h)
description: The CryptGetMessageSignerCount function returns the number of signers of a signed message.
helpviewer_keywords: ["CryptGetMessageSignerCount","CryptGetMessageSignerCount function [Security]","_crypto2_cryptgetmessagesignercount","security.cryptgetmessagesignercount","wincrypt/CryptGetMessageSignerCount"]
old-location: security\cryptgetmessagesignercount.htm
tech.root: security
ms.assetid: d18bda8b-b333-4b1e-8ed5-f8eff04b3168
ms.date: 10/24/2021
ms.keywords: CryptGetMessageSignerCount, CryptGetMessageSignerCount function [Security], _crypto2_cryptgetmessagesignercount, security.cryptgetmessagesignercount, wincrypt/CryptGetMessageSignerCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptGetMessageSignerCount
 - wincrypt/CryptGetMessageSignerCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptGetMessageSignerCount
---

# CryptGetMessageSignerCount function


## -description

The <b>CryptGetMessageSignerCount</b> function returns the number of signers of a signed message.

> [!NOTE]
> This function may return a count of duplicate signers and therefore may not be sufficient to avert attacks. We recommend using the sid (SignerIdentifier) field from SignerInfo to identify duplicate signers in a message.

## -parameters

### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbSignedBlob [in]

A pointer to a buffer containing the signed message.

### -param cbSignedBlob [in]

The size, in bytes, of the signed message.

## -returns

Returns the number of signers of a signed message, zero when there are no signers, and minus one (–1) for an error.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  error code is most commonly returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a>. Currently only PKCS_7_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.



## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>

<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>
