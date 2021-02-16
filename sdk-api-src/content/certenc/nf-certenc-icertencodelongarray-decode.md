---
UID: NF:certenc.ICertEncodeLongArray.Decode
title: ICertEncodeLongArray::Decode (certenc.h)
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded Long array and stores the resulting array of Long values in the CertEncodeLongArray object.
helpviewer_keywords: ["CCertEncodeLongArray object [Security]","Decode method","Decode","Decode method [Security]","Decode method [Security]","CCertEncodeLongArray object","Decode method [Security]","ICertEncodeLongArray interface","ICertEncodeLongArray interface [Security]","Decode method","ICertEncodeLongArray.Decode","ICertEncodeLongArray::Decode","_certsrv_icertencodelongarray_decode","certenc/ICertEncodeLongArray::Decode","security.icertencodelongarray_decode"]
old-location: security\icertencodelongarray_decode.htm
tech.root: security
ms.assetid: b0ff8e1a-c4b2-48ac-be95-228638d00e6d
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeLongArray object, Decode method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],Decode method, ICertEncodeLongArray.Decode, ICertEncodeLongArray::Decode, _certsrv_icertencodelongarray_decode, certenc/ICertEncodeLongArray::Decode, security.icertencodelongarray_decode
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
 - ICertEncodeLongArray::Decode
 - certenc/ICertEncodeLongArray::Decode
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
 - ICertEncodeLongArray.Decode
 - CCertEncodeLongArray.Decode
---

# ICertEncodeLongArray::Decode


## -description

The <b>Decode</b> method decodes an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded <b>Long</b> array and stores the resulting array of <b>Long</b> values in the <b>CertEncodeLongArray</b> object.

## -parameters

### -param strBinary [in]

An ASN.1-encoded <b>Long</b> array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method places the decoded contents of <i>strBinary</i> into the object's array of <b>Long</b> values. If the object's array already contains <b>Long</b> values, the existing content will be freed, and the array will be loaded with the decoded values.


#### Examples

For an example that uses the <b>Decode</b> method, see the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-encode">ICertEncodeLongArray::Encode</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodelongarray">ICertEncodeLongArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-encode">ICertEncodeLongArray::Encode</a>