---
UID: NF:certenc.ICertEncodeAltName.Decode
title: ICertEncodeAltName::Decode (certenc.h)
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded alternate name extension and stores the resulting array of strings in the CertEncodeAltName object.
helpviewer_keywords: ["CCertEncodeAltName object [Security]","Decode method","Decode","Decode method [Security]","Decode method [Security]","CCertEncodeAltName object","Decode method [Security]","ICertEncodeAltName interface","ICertEncodeAltName interface [Security]","Decode method","ICertEncodeAltName.Decode","ICertEncodeAltName::Decode","_certsrv_icertencodealtname_decode","certenc/ICertEncodeAltName::Decode","security.icertencodealtname_decode"]
old-location: security\icertencodealtname_decode.htm
tech.root: security
ms.assetid: 0507d3a5-b8c3-4f2e-996f-e1e32957f475
ms.date: 12/05/2018
ms.keywords: CCertEncodeAltName object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeAltName object, Decode method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],Decode method, ICertEncodeAltName.Decode, ICertEncodeAltName::Decode, _certsrv_icertencodealtname_decode, certenc/ICertEncodeAltName::Decode, security.icertencodealtname_decode
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
 - ICertEncodeAltName::Decode
 - certenc/ICertEncodeAltName::Decode
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
 - ICertEncodeAltName.Decode
 - CCertEncodeAltName.Decode
---

# ICertEncodeAltName::Decode


## -description

The <b>Decode</b> method decodes an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded alternate name extension and stores the resulting array of strings in the <b>CertEncodeAltName</b> object.

## -parameters

### -param strBinary [in]

Represents an ASN.1-encoded alternate name extension.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodealtname">ICertEncodeAltName</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodealtname-encode">ICertEncodeAltName::Encode</a>