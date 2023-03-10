---
UID: NF:certenc.ICertEncodeAltName.Encode
title: ICertEncodeAltName::Encode (certenc.h)
description: Returns an ASN.1-encoded string of the alternate name array stored in this object. The names in the object are not encoded.
helpviewer_keywords: ["CCertEncodeAltName object [Security]","Encode method","Encode","Encode method [Security]","Encode method [Security]","CCertEncodeAltName object","Encode method [Security]","ICertEncodeAltName interface","ICertEncodeAltName interface [Security]","Encode method","ICertEncodeAltName.Encode","ICertEncodeAltName::Encode","_certsrv_icertencodealtname_encode","certenc/ICertEncodeAltName::Encode","security.icertencodealtname_encode"]
old-location: security\icertencodealtname_encode.htm
tech.root: security
ms.assetid: 34136053-1c25-4f6b-8bd6-699fffb6670b
ms.date: 12/05/2018
ms.keywords: CCertEncodeAltName object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeAltName object, Encode method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],Encode method, ICertEncodeAltName.Encode, ICertEncodeAltName::Encode, _certsrv_icertencodealtname_encode, certenc/ICertEncodeAltName::Encode, security.icertencodealtname_encode
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
 - ICertEncodeAltName::Encode
 - certenc/ICertEncodeAltName::Encode
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
 - ICertEncodeAltName.Encode
 - CCertEncodeAltName.Encode
---

# ICertEncodeAltName::Encode


## -description

The <b>Encode</b> method returns an ASN.1-encoded string of the alternate name array stored in this object. The names in the object are not encoded.

Use the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-decode">Decode</a> method to decode the encoded string into an <b>CertEncodeAltName</b> object.

Before using this method, you must call both the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-reset">Reset</a> method to size the array and the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-setnameentry">SetNameEntry</a> method to set each array element.

## -parameters

### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that receives the ASN.1-encoded alternate name extension. When done, call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free <i>pbstrBinary</i>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded alternate name array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodealtname">ICertEncodeAltName</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-decode">ICertEncodeAltName::Decode</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-reset">ICertEncodeAltName::Reset</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-setnameentry">ICertEncodeAltName::SetNameEntry</a>