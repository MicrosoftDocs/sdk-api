---
UID: NF:certenc.ICertEncodeDateArray.Encode
title: ICertEncodeDateArray::Encode (certenc.h)
description: Returns an Abstract Syntax Notation One (ASN.1)-encoded string of the date array stored in this object.
helpviewer_keywords: ["CCertEncodeDateArray object [Security]","Encode method","Encode","Encode method [Security]","Encode method [Security]","CCertEncodeDateArray object","Encode method [Security]","ICertEncodeDateArray interface","ICertEncodeDateArray interface [Security]","Encode method","ICertEncodeDateArray.Encode","ICertEncodeDateArray::Encode","_certsrv_icertencodedatearray_encode","certenc/ICertEncodeDateArray::Encode","security.icertencodedatearray_encode"]
old-location: security\icertencodedatearray_encode.htm
tech.root: security
ms.assetid: 102ca165-c320-4e18-986f-7375fbc617e0
ms.date: 12/05/2018
ms.keywords: CCertEncodeDateArray object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeDateArray object, Encode method [Security],ICertEncodeDateArray interface, ICertEncodeDateArray interface [Security],Encode method, ICertEncodeDateArray.Encode, ICertEncodeDateArray::Encode, _certsrv_icertencodedatearray_encode, certenc/ICertEncodeDateArray::Encode, security.icertencodedatearray_encode
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
 - ICertEncodeDateArray::Encode
 - certenc/ICertEncodeDateArray::Encode
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
 - ICertEncodeDateArray.Encode
 - CCertEncodeDateArray.Encode
---

# ICertEncodeDateArray::Encode


## -description

The <b>Encode</b> method returns an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded string of the date array stored in this object.

Use the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-decode">Decode</a> method to decode the encoded string into an <b>CertEncodeDateArray</b> object.

Before using this method, you must call both the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-reset">Reset</a> method to size the array and the 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-setvalue">SetValue</a> method to set each array element.

## -parameters

### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded <b>Date</b> array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string that represents the <b>DATE</b> array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodedatearray">ICertEncodeDateArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-decode">ICertEncodeDateArray::Decode</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-reset">ICertEncodeDateArray::Reset</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-setvalue">ICertEncodeDateArray::SetValue</a>