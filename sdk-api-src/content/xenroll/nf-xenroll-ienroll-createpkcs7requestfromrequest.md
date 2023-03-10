---
UID: NF:xenroll.IEnroll.CreatePKCS7RequestFromRequest
title: IEnroll::CreatePKCS7RequestFromRequest (xenroll.h)
description: The CreatePKCS7RequestFromRequest method creates a PKCS
helpviewer_keywords: ["CreatePKCS7RequestFromRequest","CreatePKCS7RequestFromRequest method [Security]","CreatePKCS7RequestFromRequest method [Security]","IEnroll interface","CreatePKCS7RequestFromRequest method [Security]","IEnroll2 interface","IEnroll interface [Security]","CreatePKCS7RequestFromRequest method","IEnroll.CreatePKCS7RequestFromRequest","IEnroll2 interface [Security]","CreatePKCS7RequestFromRequest method","IEnroll2::CreatePKCS7RequestFromRequest","IEnroll::CreatePKCS7RequestFromRequest","security.ienroll4_createpkcs7requestfromrequest","xenroll/IEnroll2::CreatePKCS7RequestFromRequest","xenroll/IEnroll::CreatePKCS7RequestFromRequest"]
old-location: security\ienroll4_createpkcs7requestfromrequest.htm
tech.root: security
ms.assetid: f1d2df72-bedc-45e5-8c0a-a731845d4487
ms.date: 12/05/2018
ms.keywords: CreatePKCS7RequestFromRequest, CreatePKCS7RequestFromRequest method [Security], CreatePKCS7RequestFromRequest method [Security],IEnroll interface, CreatePKCS7RequestFromRequest method [Security],IEnroll2 interface, IEnroll interface [Security],CreatePKCS7RequestFromRequest method, IEnroll.CreatePKCS7RequestFromRequest, IEnroll2 interface [Security],CreatePKCS7RequestFromRequest method, IEnroll2::CreatePKCS7RequestFromRequest, IEnroll::CreatePKCS7RequestFromRequest, security.ienroll4_createpkcs7requestfromrequest, xenroll/IEnroll2::CreatePKCS7RequestFromRequest, xenroll/IEnroll::CreatePKCS7RequestFromRequest
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
 - IEnroll::CreatePKCS7RequestFromRequest
 - xenroll/IEnroll::CreatePKCS7RequestFromRequest
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
 - IEnroll.CreatePKCS7RequestFromRequest
 - IEnroll2.CreatePKCS7RequestFromRequest
---

# IEnroll::CreatePKCS7RequestFromRequest


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>CreatePKCS7RequestFromRequest</b> method creates a PKCS #7 request from an existing certificate request. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param pRequest [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the existing request.

### -param pSigningCertContext [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that represents the certificate used to sign the request.

### -param pPkcs7Blob [out]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that receives the returned PKCS  #7 certificate request.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>