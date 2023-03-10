---
UID: NF:xenroll.IEnroll.createPKCS10WStr
title: IEnroll::createPKCS10WStr (xenroll.h)
description: Creates a base64-encoded PKCS (IEnroll.createPKCS10WStr)
helpviewer_keywords: ["IEnroll interface [Security]","createPKCS10WStr method","IEnroll.createPKCS10WStr","IEnroll::createPKCS10WStr","createPKCS10WStr","createPKCS10WStr method [Security]","createPKCS10WStr method [Security]","IEnroll interface","security.ienroll4_createpkcs10wstr","xenroll/IEnroll::createPKCS10WStr"]
old-location: security\ienroll4_createpkcs10wstr.htm
tech.root: security
ms.assetid: ebbcc9ad-9f87-4abe-963b-38c57a60e45e
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],createPKCS10WStr method, IEnroll.createPKCS10WStr, IEnroll::createPKCS10WStr, createPKCS10WStr, createPKCS10WStr method [Security], createPKCS10WStr method [Security],IEnroll interface, security.ienroll4_createpkcs10wstr, xenroll/IEnroll::createPKCS10WStr
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll::createPKCS10WStr
 - xenroll/IEnroll::createPKCS10WStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.createPKCS10WStr
---

# IEnroll::createPKCS10WStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createPKCS10WStr</b> method creates a base64-encoded PKCS #10 <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

 This base64-encoded PKCS #10 certificate request (in <b>BSTR</b> form) can be submitted to a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> to request  that a certificate be issued to the person or entity whose information it contains.

## -parameters

### -param DNName [in]

A null-terminated Unicode string that contains the distinguished name (DN) of the entity for which the request is being made. In this parameter, the DN name must follow the <a href="/windows/desktop/SecGloss/x-gly">X.500</a> naming convention. For example "CN=User, O=Microsoft". If a two-letter prefix does not exist, an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) may be provided instead.

### -param Usage [in]

A null-terminated Unicode string that contains an OID that describes the purpose of the certificate being generated. For example, Individual or Commercial Authenticode certificate, or Client Authentication. You can also specify multiple OIDs separated by a comma.

The  OID is passed through to the PKCS #10 request. For general extensibility and ease of understanding, the control does not attempt to understand specific-purpose OIDs. Therefore if you specify a Client Authentication OID, the generated key will still be a signature key, not an <a href="/windows/desktop/SecGloss/e-gly">exchange key</a>.

### -param pPkcs10Blob [out]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> that receives the base64-encoded PKCS10 certificate request.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

 If the method succeeds, the method returns S_OK and <i>pPkcs10Blob</i> contains a base64-encoded PKCS #10 request that can be directly posted to a web server for processing.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

By default, the Microsoft Base Cryptographic Provider is used, PROV_RSA_FULL is the provider type, a signature key is created, and a unique new key set is created.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
