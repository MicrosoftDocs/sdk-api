---
UID: NF:certenc.ICertEncodeDateArray.Decode
title: ICertEncodeDateArray::Decode (certenc.h)
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded date array and stores the resulting array of date values in the CertEncodeDateArray object.
helpviewer_keywords: ["CCertEncodeDateArray object [Security]","Decode method","Decode","Decode method [Security]","Decode method [Security]","CCertEncodeDateArray object","Decode method [Security]","ICertEncodeDateArray interface","ICertEncodeDateArray interface [Security]","Decode method","ICertEncodeDateArray.Decode","ICertEncodeDateArray::Decode","_certsrv_icertencodedatearray_decode","certenc/ICertEncodeDateArray::Decode","security.icertencodedatearray_decode"]
old-location: security\icertencodedatearray_decode.htm
tech.root: security
ms.assetid: 79937ef7-4b1a-4132-9ef4-23b2857c7fac
ms.date: 12/05/2018
ms.keywords: CCertEncodeDateArray object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeDateArray object, Decode method [Security],ICertEncodeDateArray interface, ICertEncodeDateArray interface [Security],Decode method, ICertEncodeDateArray.Decode, ICertEncodeDateArray::Decode, _certsrv_icertencodedatearray_decode, certenc/ICertEncodeDateArray::Decode, security.icertencodedatearray_decode
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
 - ICertEncodeDateArray::Decode
 - certenc/ICertEncodeDateArray::Decode
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
 - ICertEncodeDateArray.Decode
 - CCertEncodeDateArray.Decode
---

# ICertEncodeDateArray::Decode


## -description

The <b>Decode</b> method decodes an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded date array and stores the resulting array of date values in the <b>CertEncodeDateArray</b> object.

## -parameters

### -param strBinary [in]

An ASN.1-encoded <b>DATE</b> array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This method places the decoded contents of <i>strBinary</i> into the object's array of date values. If the object's array already contains date values, this existing content will be freed, and the array will be loaded with the decoded values.


#### Examples

For an example that uses the <b>Decode</b> method, see the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-encode">ICertEncodeDateArray::Encode</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodedatearray">ICertEncodeDateArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-encode">ICertEncodeDateArray::Encode</a>