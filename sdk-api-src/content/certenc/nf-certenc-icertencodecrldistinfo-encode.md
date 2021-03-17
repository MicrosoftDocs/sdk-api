---
UID: NF:certenc.ICertEncodeCRLDistInfo.Encode
title: ICertEncodeCRLDistInfo::Encode (certenc.h)
description: Performs Abstract Syntax Notation One (ASN.1) encoding on a certificate revocation list (CRL) distribution information array stored in the COM object and returns the ASN.1-encoded extension.
helpviewer_keywords: ["CCertEncodeCRLDistInfo object [Security]","Encode method","Encode","Encode method [Security]","Encode method [Security]","CCertEncodeCRLDistInfo object","Encode method [Security]","ICertEncodeCRLDistInfo interface","ICertEncodeCRLDistInfo interface [Security]","Encode method","ICertEncodeCRLDistInfo.Encode","ICertEncodeCRLDistInfo::Encode","_certsrv_icertencodecrldistinfo_encode","certenc/ICertEncodeCRLDistInfo::Encode","security.icertencodecrldistinfo_encode"]
old-location: security\icertencodecrldistinfo_encode.htm
tech.root: security
ms.assetid: 46520e3a-1f15-4d1c-9f44-b9b420fb4f25
ms.date: 12/05/2018
ms.keywords: CCertEncodeCRLDistInfo object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeCRLDistInfo object, Encode method [Security],ICertEncodeCRLDistInfo interface, ICertEncodeCRLDistInfo interface [Security],Encode method, ICertEncodeCRLDistInfo.Encode, ICertEncodeCRLDistInfo::Encode, _certsrv_icertencodecrldistinfo_encode, certenc/ICertEncodeCRLDistInfo::Encode, security.icertencodecrldistinfo_encode
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
 - ICertEncodeCRLDistInfo::Encode
 - certenc/ICertEncodeCRLDistInfo::Encode
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
 - ICertEncodeCRLDistInfo.Encode
 - CCertEncodeCRLDistInfo.Encode
---

# ICertEncodeCRLDistInfo::Encode


## -description

The <b>Encode</b> method performs <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding on a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information array stored in the COM object and returns the ASN.1-encoded extension.

 Before using this method, you must call the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-reset">Reset</a> method to size the array and the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnamecount">SetNameCount</a> and 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnameentry">SetNameEntry</a> methods to set each element in each distribution point structure.

## -parameters

### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded CRL distribution information extension. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string that represents the CRL distribution information array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodecrldistinfo">ICertEncodeCRLDistInfo</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-reset">ICertEncodeCRLDistInfo::Reset</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnamecount">ICertEncodeCRLDistInfo::SetNameCount</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodecrldistinfo-setnameentry">ICertEncodeCRLDistInfo::SetNameEntry</a>