---
UID: NF:certenc.ICertEncodeBitString.Encode
title: ICertEncodeBitString::Encode (certenc.h)
description: Performs Abstract Syntax Notation One (ASN.1) encoding on a given bit string.
helpviewer_keywords: ["CCertEncodeBitString object [Security]","Encode method","Encode","Encode method [Security]","Encode method [Security]","CCertEncodeBitString object","Encode method [Security]","ICertEncodeBitString interface","ICertEncodeBitString interface [Security]","Encode method","ICertEncodeBitString.Encode","ICertEncodeBitString::Encode","_certsrv_icertencodebitstring_encode","certenc/ICertEncodeBitString::Encode","security.icertencodebitstring_encode"]
old-location: security\icertencodebitstring_encode.htm
tech.root: security
ms.assetid: 2dc74ab4-8f40-4e0d-a18e-ba9c99d5bf94
ms.date: 12/05/2018
ms.keywords: CCertEncodeBitString object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeBitString object, Encode method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],Encode method, ICertEncodeBitString.Encode, ICertEncodeBitString::Encode, _certsrv_icertencodebitstring_encode, certenc/ICertEncodeBitString::Encode, security.icertencodebitstring_encode
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeBitString::Encode
 - certenc/ICertEncodeBitString::Encode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeBitString.Encode
 - CCertEncodeBitString.Encode
---

# ICertEncodeBitString::Encode


## -description

The <b>Encode</b> method performs <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding on a given bit string.

## -parameters

### -param BitCount [in]

The number of bits in <i>strBitString</i>.

### -param strBitString [in]

The bit string to encode.

### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded bit string. When you have finished using this <b>BSTR</b>, call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to free <i>pbstrBinary</i>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded bit string.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodebitstring">ICertEncodeBitString</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodebitstring-decode">ICertEncodeBitString::Decode</a>