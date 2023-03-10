---
UID: NF:certenc.ICertEncodeStringArray.Encode
title: ICertEncodeStringArray::Encode (certenc.h)
description: Returns an ASN.1-encoded string of the string array stored in this object.
helpviewer_keywords: ["CCertEncodeStringArray object [Security]","Encode method","Encode","Encode method [Security]","Encode method [Security]","CCertEncodeStringArray object","Encode method [Security]","ICertEncodeStringArray interface","ICertEncodeStringArray interface [Security]","Encode method","ICertEncodeStringArray.Encode","ICertEncodeStringArray::Encode","_certsrv_icertencodestringarray_encode","certenc/ICertEncodeStringArray::Encode","security.icertencodestringarray_encode"]
old-location: security\icertencodestringarray_encode.htm
tech.root: security
ms.assetid: d8fc51ea-4d83-402a-a4ac-ce55d385905c
ms.date: 12/05/2018
ms.keywords: CCertEncodeStringArray object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeStringArray object, Encode method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],Encode method, ICertEncodeStringArray.Encode, ICertEncodeStringArray::Encode, _certsrv_icertencodestringarray_encode, certenc/ICertEncodeStringArray::Encode, security.icertencodestringarray_encode
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
 - ICertEncodeStringArray::Encode
 - certenc/ICertEncodeStringArray::Encode
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
 - ICertEncodeStringArray.Encode
 - CCertEncodeStringArray.Encode
---

# ICertEncodeStringArray::Encode


## -description

The <b>Encode</b> method returns an ASN.1-encoded string of the string array stored in this object.

Use the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-decode">Decode</a> method to decode the encoded string into an <b>CertEncodeStringArray</b> object.

 Before using this method, you must call the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-reset">Reset</a> to size the array and the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-setvalue">SetValue</a> method to set each string in the array.

## -parameters

### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded string array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodestringarray">ICertEncodeStringArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-decode">ICertEncodeStringArray::Decode</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-reset">ICertEncodeStringArray::Reset</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-setvalue">ICertEncodeStringArray::SetValue</a>