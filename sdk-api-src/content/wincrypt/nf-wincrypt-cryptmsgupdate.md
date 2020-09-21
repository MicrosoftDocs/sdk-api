---
UID: NF:wincrypt.CryptMsgUpdate
title: CryptMsgUpdate function (wincrypt.h)
description: Adds contents to a cryptographic message.
helpviewer_keywords: ["CryptMsgUpdate","CryptMsgUpdate function [Security]","_crypto2_cryptmsgupdate","security.cryptmsgupdate","wincrypt/CryptMsgUpdate"]
old-location: security\cryptmsgupdate.htm
tech.root: security
ms.assetid: d27d75f0-1646-4926-b375-59e52b00326c
ms.date: 12/05/2018
ms.keywords: CryptMsgUpdate, CryptMsgUpdate function [Security], _crypto2_cryptmsgupdate, security.cryptmsgupdate, wincrypt/CryptMsgUpdate
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
 - CryptMsgUpdate
 - wincrypt/CryptMsgUpdate
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
 - CryptMsgUpdate
---

# CryptMsgUpdate function


## -description

The <b>CryptMsgUpdate</b> function adds contents to a cryptographic message. The use of this function allows messages to be constructed piece by piece through repetitive calls of <b>CryptMsgUpdate</b>. The added message content is either encoded or decoded depending on whether the message was opened with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>.

## -parameters

### -param hCryptMsg [in]

Cryptographic message handle of the message to be updated.

### -param pbData [in]

A pointer to the buffer holding the data to be encoded or decoded.

### -param cbData [in]

Number of bytes of data in the <i>pbData</i> buffer.

### -param fFinal [in]

Indicates that the last block of data for encoding or decoding is being processed. Correct usage of this flag is dependent upon whether the message being processed has detached data. The inclusion of detached data in a message is indicated by setting <i>dwFlags</i> to CMSG_DETACHED_FLAG in the call to the function that opened the message. 




If CMSG_DETACHED_FLAG was not set and the message was opened using either 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>, <i>fFinal</i> is set to <b>TRUE</b>, and <b>CryptMsgUpdate</b> is only called once.

If the CMSG_DETACHED_FLAG flag was set and a message is opened using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>, <i>fFinal</i> is set to <b>TRUE</b> only on the last call to <b>CryptMsgUpdate</b>.

If the CMSG_DETACHED_FLAG flag was set and a message is opened using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>, <i>fFinal</i> is set to <b>TRUE</b> when the header is processed by a single call to <b>CryptMsgUpdate</b>. It is set to <b>FALSE</b> while processing the detached data in subsequent calls to <b>CryptMsgUpdate</b> until the last detached data block is to be processed. On the last call to <b>CryptMsgUpdate</b>, it is set to <b>TRUE</b>.

When detached data is decoded, the header and the content of a message are contained in different BLOBs. Each BLOB requires that <i>fFinal</i> be set to <b>TRUE</b> when the last call to the function is made for that BLOB.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Errors encountered in the application defined callback function specified by <i>pStreamInfo</i> in 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> might be propagated to <b>CryptMsgUpdate</b> if streaming is used. If this happens, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> is not called by <b>CryptMsgUpdate</b> after the callback function returns, which preserves any errors encountered under the control of the application. It is the responsibility of the callback function (or one of the APIs that it calls) to call <b>SetLastError</b> if an error occurs while the application is processing the streamed data.

The following table lists the error codes most commonly returned by the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_INVALID_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The message type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_MSG_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered doing a cryptographic operation.

</td>
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
<dt><b>CRYPT_E_UNEXPECTED_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
The message is not encoded as expected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
</dl>
</td>
<td width="60%">
The cryptographic algorithm is unknown.

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
 

Propagated errors might be encountered from any of the following functions:<ul>
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
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencrypt">CryptEncrypt</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>
</li>
</ul>


If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentodecode">CryptMsgOpenToDecode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Low-level Message Functions</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>