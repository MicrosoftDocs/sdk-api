---
UID: NF:certenc.ICertEncodeStringArray.Decode
title: ICertEncodeStringArray::Decode (certenc.h)
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded string array and stores the resulting array of strings in the CertEncodeStringArray object.
helpviewer_keywords: ["CCertEncodeStringArray object [Security]","Decode method","Decode","Decode method [Security]","Decode method [Security]","CCertEncodeStringArray object","Decode method [Security]","ICertEncodeStringArray interface","ICertEncodeStringArray interface [Security]","Decode method","ICertEncodeStringArray.Decode","ICertEncodeStringArray::Decode","_certsrv_icertencodestringarray_decode","certenc/ICertEncodeStringArray::Decode","security.icertencodestringarray_decode"]
old-location: security\icertencodestringarray_decode.htm
tech.root: security
ms.assetid: 35799b54-2c04-4bb4-a227-d2902b2379ec
ms.date: 12/05/2018
ms.keywords: CCertEncodeStringArray object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeStringArray object, Decode method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],Decode method, ICertEncodeStringArray.Decode, ICertEncodeStringArray::Decode, _certsrv_icertencodestringarray_decode, certenc/ICertEncodeStringArray::Decode, security.icertencodestringarray_decode
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
 - ICertEncodeStringArray::Decode
 - certenc/ICertEncodeStringArray::Decode
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
 - ICertEncodeStringArray.Decode
 - CCertEncodeStringArray.Decode
---

# ICertEncodeStringArray::Decode


## -description

The <b>Decode</b> method decodes an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded string array and stores the resulting array of strings in the <b>CertEncodeStringArray</b> object.

## -parameters

### -param strBinary [in]

An ASN.1-encoded string array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method will place the decoded contents of <i>strBinary</i> into the object's array of strings. If the object's array already contains strings, this existing content will be freed, and the array will be loaded with the decoded values.


#### Examples

For an example that uses the <b>Decode</b> method, see the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-encode">ICertEncodeStringArray::Encode</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodestringarray">ICertEncodeStringArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-encode">ICertEncodeStringArray::Encode</a>