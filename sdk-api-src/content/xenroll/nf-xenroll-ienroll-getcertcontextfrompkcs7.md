---
UID: NF:xenroll.IEnroll.getCertContextFromPKCS7
title: IEnroll::getCertContextFromPKCS7 (xenroll.h)
description: Retrieves a certificate context based on a PKCS
helpviewer_keywords: ["IEnroll interface [Security]","getCertContextFromPKCS7 method","IEnroll.getCertContextFromPKCS7","IEnroll2 interface [Security]","getCertContextFromPKCS7 method","IEnroll2::getCertContextFromPKCS7","IEnroll::getCertContextFromPKCS7","getCertContextFromPKCS7","getCertContextFromPKCS7 method [Security]","getCertContextFromPKCS7 method [Security]","IEnroll interface","getCertContextFromPKCS7 method [Security]","IEnroll2 interface","security.ienroll4_getcertcontextfrompkcs7","xenroll/IEnroll2::getCertContextFromPKCS7","xenroll/IEnroll::getCertContextFromPKCS7"]
old-location: security\ienroll4_getcertcontextfrompkcs7.htm
tech.root: security
ms.assetid: 3781729d-8b08-41b5-8ff4-1de19fc4ee2e
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],getCertContextFromPKCS7 method, IEnroll.getCertContextFromPKCS7, IEnroll2 interface [Security],getCertContextFromPKCS7 method, IEnroll2::getCertContextFromPKCS7, IEnroll::getCertContextFromPKCS7, getCertContextFromPKCS7, getCertContextFromPKCS7 method [Security], getCertContextFromPKCS7 method [Security],IEnroll interface, getCertContextFromPKCS7 method [Security],IEnroll2 interface, security.ienroll4_getcertcontextfrompkcs7, xenroll/IEnroll2::getCertContextFromPKCS7, xenroll/IEnroll::getCertContextFromPKCS7
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
 - IEnroll::getCertContextFromPKCS7
 - xenroll/IEnroll::getCertContextFromPKCS7
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
 - IEnroll.getCertContextFromPKCS7
 - IEnroll2.getCertContextFromPKCS7
---

# IEnroll::getCertContextFromPKCS7


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertContextFromPKCS7</b> method retrieves a  certificate context based on a  PKCS #7 message that was  issued in response to a PKCS #10 certificate request.

This method retrieves the context for the single certificate that was issued even though a PKCS #7 message may contain many certificates specifying the certification chain of authority that issued the certificate.

This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param pBlobPKCS7 [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the PKCS #7.

## -returns

The return value is a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> representing the certificate context, or <b>NULL</b> if the method fails.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>