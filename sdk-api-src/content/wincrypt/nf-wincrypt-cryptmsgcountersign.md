---
UID: NF:wincrypt.CryptMsgCountersign
title: CryptMsgCountersign function (wincrypt.h)
description: Countersigns an existing signature in a message.
helpviewer_keywords: ["CryptMsgCountersign","CryptMsgCountersign function [Security]","_crypto2_cryptmsgcountersign","security.cryptmsgcountersign","wincrypt/CryptMsgCountersign"]
old-location: security\cryptmsgcountersign.htm
tech.root: security
ms.assetid: ebf76664-bca6-462d-b519-2b60f435d8ef
ms.date: 12/05/2018
ms.keywords: CryptMsgCountersign, CryptMsgCountersign function [Security], _crypto2_cryptmsgcountersign, security.cryptmsgcountersign, wincrypt/CryptMsgCountersign
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
 - CryptMsgCountersign
 - wincrypt/CryptMsgCountersign
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
 - CryptMsgCountersign
---

# CryptMsgCountersign function


## -description

The <b>CryptMsgCountersign</b> function countersigns an existing signature in a message. <a href="/windows/desktop/SecGloss/c-gly">Countersignatures</a> are used to sign an existing signature's encrypted <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the message. Countersignatures can be used for various purposes including time stamping a message.

## -parameters

### -param hCryptMsg [in, out]

Cryptographic message handle to be used.

### -param dwIndex [in]

Zero-based index of the signer in the signed or signed-and-enveloped message to be countersigned.

### -param cCountersigners [in]

Number of countersigners in the <i>rgCountersigners</i> array.

### -param rgCountersigners [in]

Array of countersigners' 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

An error can be propagated from
								<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersignencoded">CryptMsgCountersignEncoded</a>.

The following error codes are returned most often.



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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified area is not large enough to hold the returned data.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcountersignencoded">CryptMsgCountersignEncoded</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded">CryptMsgVerifyCountersignatureEncoded</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>