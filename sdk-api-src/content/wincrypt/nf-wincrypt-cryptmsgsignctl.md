---
UID: NF:wincrypt.CryptMsgSignCTL
title: CryptMsgSignCTL function (wincrypt.h)
description: The CryptMsgSignCTL function creates a signed message containing an encoded CTL.
helpviewer_keywords: ["CryptMsgSignCTL","CryptMsgSignCTL function [Security]","_crypto2_cryptmsgsignctl","security.cryptmsgsignctl","wincrypt/CryptMsgSignCTL"]
old-location: security\cryptmsgsignctl.htm
tech.root: security
ms.assetid: 85ae8ce3-d0a7-4fcb-beaa-ede09d30930e
ms.date: 12/05/2018
ms.keywords: CryptMsgSignCTL, CryptMsgSignCTL function [Security], _crypto2_cryptmsgsignctl, security.cryptmsgsignctl, wincrypt/CryptMsgSignCTL
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
 - CryptMsgSignCTL
 - wincrypt/CryptMsgSignCTL
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
 - CryptMsgSignCTL
---

# CryptMsgSignCTL function


## -description

The <b>CryptMsgSignCTL</b> function creates a signed message containing an encoded CTL.

## -parameters

### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCtlContent [in]

The encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> that can be a member of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure or can be created using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function.

### -param cbCtlContent [in]

The size, in bytes, of the content pointed to by <i>pbCtlContent</i>.

### -param pSignInfo [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a> structure containing an array of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures.

The message can be encoded without signers if the <b>cbSize</b> member of the structure is set to the size of the structure and all of the other members are set to zero.

### -param dwFlags [in]

If CMS_PKCS7 is defined, can be set to CMSG_CMS_ENCAPSULATED_CTL_FLAG to encode a CMS compatible V3 SignedData message.

### -param pbEncoded [out]

A pointer to a buffer to receives the encoded message.

This parameter can be <b>NULL</b> to get the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> specifying the size, in bytes, of the <i>pbEncoded</i> buffer. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. This function can return errors propagated from calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgencodeandsignctl">CryptMsgEncodeAndSignCTL</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Verification Functions Using CTLs</a>