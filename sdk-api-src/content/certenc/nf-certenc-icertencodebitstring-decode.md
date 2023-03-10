---
UID: NF:certenc.ICertEncodeBitString.Decode
title: ICertEncodeBitString::Decode (certenc.h)
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded bit string and stores the resulting bit string in this object.
helpviewer_keywords: ["CCertEncodeBitString object [Security]","Decode method","Decode","Decode method [Security]","Decode method [Security]","CCertEncodeBitString object","Decode method [Security]","ICertEncodeBitString interface","ICertEncodeBitString interface [Security]","Decode method","ICertEncodeBitString.Decode","ICertEncodeBitString::Decode","_certsrv_icertencodebitstring_decode","certenc/ICertEncodeBitString::Decode","security.icertencodebitstring_decode"]
old-location: security\icertencodebitstring_decode.htm
tech.root: security
ms.assetid: 65856db4-97db-4c9b-ac12-1a9262c7b4e9
ms.date: 12/05/2018
ms.keywords: CCertEncodeBitString object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeBitString object, Decode method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],Decode method, ICertEncodeBitString.Decode, ICertEncodeBitString::Decode, _certsrv_icertencodebitstring_decode, certenc/ICertEncodeBitString::Decode, security.icertencodebitstring_decode
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
 - ICertEncodeBitString::Decode
 - certenc/ICertEncodeBitString::Decode
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
 - ICertEncodeBitString.Decode
 - CCertEncodeBitString.Decode
---

# ICertEncodeBitString::Decode


## -description

The <b>Decode</b> method decodes an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded bit string and stores the resulting bit string in this object. You can then call the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodebitstring-getbitcount">ICertEncodeBitString::GetBitCount</a> and 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodebitstring-getbitstring">ICertEncodeBitString::GetBitString</a> methods to retrieve the bit string and its size.

## -parameters

### -param strBinary [in]

An ASN.1-encoded bit string.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Use this method to decode an encoded bit string.


#### Examples

For an example that calls the <b>Decode</b> method, see the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodebitstring-encode">ICertEncodeBitString::Encode</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodebitstring">ICertEncodeBitString</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodebitstring-encode">ICertEncodeBitString::Encode</a>