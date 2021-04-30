---
UID: NF:certenc.ICertEncodeLongArray.Encode
title: ICertEncodeLongArray::Encode (certenc.h)
description: Returns an ASN.1-encoded string of the LONG array stored in this object.
helpviewer_keywords: ["CCertEncodeLongArray object [Security]","Encode method","Encode","Encode method [Security]","Encode method [Security]","CCertEncodeLongArray object","Encode method [Security]","ICertEncodeLongArray interface","ICertEncodeLongArray interface [Security]","Encode method","ICertEncodeLongArray.Encode","ICertEncodeLongArray::Encode","_certsrv_icertencodelongarray_encode","certenc/ICertEncodeLongArray::Encode","security.icertencodelongarray_encode"]
old-location: security\icertencodelongarray_encode.htm
tech.root: security
ms.assetid: e2cf6e69-2431-4a97-86f1-9e1546aa6c08
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeLongArray object, Encode method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],Encode method, ICertEncodeLongArray.Encode, ICertEncodeLongArray::Encode, _certsrv_icertencodelongarray_encode, certenc/ICertEncodeLongArray::Encode, security.icertencodelongarray_encode
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
 - ICertEncodeLongArray::Encode
 - certenc/ICertEncodeLongArray::Encode
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
 - ICertEncodeLongArray.Encode
 - CCertEncodeLongArray.Encode
---

# ICertEncodeLongArray::Encode


## -description

The <b>Encode</b> method returns an ASN.1-encoded string of the <b>LONG</b> array stored in this object.

Use the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-decode">Decode</a> method to decode the encoded string into an <b>CertEncodeLongArray</b> object.

Before calling the <b>Encode</b> method, you must call the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-reset">Reset</a> method to size the array and the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-setvalue">SetValue</a> method to set each <b>LONG</b> value in the array.

## -parameters

### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded <b>LONG</b> array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is the ASN.1-encoded <b>LONG</b> array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodelongarray">ICertEncodeLongArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-decode">ICertEncodeLongArray::Decode</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-reset">ICertEncodeLongArray::Reset</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-setvalue">ICertEncodeLongArray::SetValue</a>