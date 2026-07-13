---
UID: NF:xenroll.IEnroll.acceptPKCS7Blob
title: IEnroll::acceptPKCS7Blob (xenroll.h)
description: Accepts and processes a PKCS (IEnroll.acceptPKCS7Blob)
helpviewer_keywords: ["IEnroll interface [Security]","acceptPKCS7Blob method","IEnroll.acceptPKCS7Blob","IEnroll::acceptPKCS7Blob","acceptPKCS7Blob","acceptPKCS7Blob method [Security]","acceptPKCS7Blob method [Security]","IEnroll interface","security.ienroll4_acceptpkcs7blob","xenroll/IEnroll::acceptPKCS7Blob"]
old-location: security\ienroll4_acceptpkcs7blob.htm
tech.root: security
ms.assetid: 8772f528-2c33-48f4-bb0c-cfde91cf2fba
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],acceptPKCS7Blob method, IEnroll.acceptPKCS7Blob, IEnroll::acceptPKCS7Blob, acceptPKCS7Blob, acceptPKCS7Blob method [Security], acceptPKCS7Blob method [Security],IEnroll interface, security.ienroll4_acceptpkcs7blob, xenroll/IEnroll::acceptPKCS7Blob
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
 - IEnroll::acceptPKCS7Blob
 - xenroll/IEnroll::acceptPKCS7Blob
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
 - IEnroll.acceptPKCS7Blob
---

# IEnroll::acceptPKCS7Blob


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptPKCS7Blob</b> method accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param pBlobPKCS7 [in]

Represents the base64-encoded PKCS #7 containing the certificate and the chain of certificates identifying the issuer.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 will be accepted.

## -remarks

The PKCS #7 input as a parameter for <b>acceptPKCS7Blob</b> contains the request certificate and the chain of certificates identifying the issuer of the certificate. Typically, but not always, the chain of certificates does not include the root. The PKCS #7 can be in base64-encoded, binary, or <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate format (with or without the "begin cert"  and  "end cert" tags). The certificate and the associated keys generated for it are put in the MY store. A <a href="/windows/desktop/SecGloss/r-gly">root certificate</a> is placed in the ROOT store, and the rest of the chain of certificates is placed in the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) store. If any ROOT certificates found in the PKCS #7 are accepted, Crypt32 will notify the user that a ROOT certificate is being added to the user's store. The user has the option of declining the ROOT certificate. This option is provided so that the user can decline to place an untrusted root in the ROOT store. Declining to place the ROOT in the ROOT store will not cause Certificate Enrollment Control to fail acceptance.


By default, the MY, CA, ROOT, and REQUEST system stores are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">MyStoreNameWStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
