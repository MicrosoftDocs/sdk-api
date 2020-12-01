---
UID: NF:wincrypt.CryptMsgEncodeAndSignCTL
title: CryptMsgEncodeAndSignCTL function (wincrypt.h)
description: The CryptMsgEncodeAndSignCTL function encodes a CTL and creates a signed message containing the encoded CTL.This function first encodes the CTL pointed to by pCtlInfo and then calls CryptMsgSignCTL to sign the encoded message.
helpviewer_keywords: ["CryptMsgEncodeAndSignCTL","CryptMsgEncodeAndSignCTL function [Security]","_crypto2_cryptmsgencodeandsignctl","security.cryptmsgencodeandsignctl","wincrypt/CryptMsgEncodeAndSignCTL"]
old-location: security\cryptmsgencodeandsignctl.htm
tech.root: security
ms.assetid: 5c0e9e2e-a50d-45d0-b51d-065784d1d912
ms.date: 12/05/2018
ms.keywords: CryptMsgEncodeAndSignCTL, CryptMsgEncodeAndSignCTL function [Security], _crypto2_cryptmsgencodeandsignctl, security.cryptmsgencodeandsignctl, wincrypt/CryptMsgEncodeAndSignCTL
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
 - CryptMsgEncodeAndSignCTL
 - wincrypt/CryptMsgEncodeAndSignCTL
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
 - CryptMsgEncodeAndSignCTL
---

# CryptMsgEncodeAndSignCTL function


## -description

The <b>CryptMsgEncodeAndSignCTL</b> function encodes a <a href="/windows/desktop/SecGloss/c-gly">CTL</a> and creates a signed message containing the encoded CTL.

This function first encodes the CTL pointed to by <i>pCtlInfo</i> and then calls 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgsignctl">CryptMsgSignCTL</a> to sign the encoded message.

## -parameters

### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCtlInfo [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> structure containing the CTL to be encoded and signed.

### -param pSignInfo [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a> structure that contains an array of a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a> structures.

The message can be encoded without signers if the <b>cbSize</b> member of the structure is set to the size of the structure and all of the other members are set to zero.

### -param dwFlags [in]

CMSG_ENCODE_SORTED_CTL_FLAG is set if the CTL entries are to be sorted before encoding. This flag is set if the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinsortedctl">CertFindSubjectInSortedCTL</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsubjectinsortedctl">CertEnumSubjectInSortedCTL</a> functions will be called.

CMSG_ENCODE_HASHED_SUBJECT_IDENTIFIER_FLAG is set if CMSG_ENCODE_SORTED_CTL_FLAG is set, and the identifier for the TrustedSubjects is a hash, such as MD5 or SHA1.

If CMS_PKCS7 is defined, <i>dwFlags</i> can be set to CMSG_CMS_ENCAPSULATED_CTL_FLAG to encode a CMS compatible V3 SignedData message.

### -param pbEncoded [out]

A pointer to a buffer that receives the encoded, signed message created.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the <i>pbEncoded</i> buffer. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Errors can be propagated from calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgupdate">CryptMsgUpdate</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signed_encode_info">CMSG_SIGNED_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsubjectinsortedctl">CertEnumSubjectInSortedCTL</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinsortedctl">CertFindSubjectInSortedCTL</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgsignctl">CryptMsgSignCTL</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Verification Functions Using CTLs</a>