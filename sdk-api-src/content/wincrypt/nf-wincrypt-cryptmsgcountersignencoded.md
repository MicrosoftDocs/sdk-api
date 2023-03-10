---
UID: NF:wincrypt.CryptMsgCountersignEncoded
title: CryptMsgCountersignEncoded function (wincrypt.h)
description: Countersigns an existing PKCS
helpviewer_keywords: ["CryptMsgCountersignEncoded","CryptMsgCountersignEncoded function [Security]","_crypto2_cryptmsgcountersignencoded","security.cryptmsgcountersignencoded","wincrypt/CryptMsgCountersignEncoded"]
old-location: security\cryptmsgcountersignencoded.htm
tech.root: security
ms.assetid: d9fd734b-e14d-4392-ac88-5565aefbedb4
ms.date: 12/05/2018
ms.keywords: CryptMsgCountersignEncoded, CryptMsgCountersignEncoded function [Security], _crypto2_cryptmsgcountersignencoded, security.cryptmsgcountersignencoded, wincrypt/CryptMsgCountersignEncoded
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CryptMsgCountersignEncoded
 - wincrypt/CryptMsgCountersignEncoded
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
 - CryptMsgCountersignEncoded
---

# CryptMsgCountersignEncoded function


## -description

The <b>CryptMsgCountersignEncoded</b> function countersigns an existing PKCS #7 message signature. The <i>pbCountersignature</i> <b>BYTE</b> buffer it creates is a PKCS #7 encoded SignerInfo that can be used as an unauthenticated <a href="/windows/desktop/SecGloss/c-gly">Countersignature</a> attribute of a PKCS #9 signed-data or signed-and-enveloped-data message.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param pbSignerInfo [in]

A pointer to the encoded SignerInfo that is to be countersigned.

### -param cbSignerInfo [in]

Count, in bytes, of the encoded SignerInfo data.

### -param cCountersigners [in]

Number of countersigners in the <i>rgCountersigners</i> array.

### -param rgCountersigners [in]

Array of countersigners' 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures.

### -param pbCountersignature [out]

A pointer to a buffer to receive an encoded PKCS #9 <a href="/windows/desktop/SecGloss/c-gly">countersignature</a> attribute.

On input, this parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbCountersignature [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pbCountersignature</i> parameter. When the function returns, the variable pointed to by the <i>pcbCountersignature</i> parameter contains the number of bytes stored in the buffer.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_OID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The object identifier is badly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
</table>
 

Propagated errors might be returned from one of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>
</li>
</ul>
If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersign">CryptMsgCountersign</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded">CryptMsgVerifyCountersignatureEncoded</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>