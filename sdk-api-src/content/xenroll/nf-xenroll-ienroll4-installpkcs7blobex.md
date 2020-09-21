---
UID: NF:xenroll.IEnroll4.InstallPKCS7BlobEx
title: IEnroll4::InstallPKCS7BlobEx (xenroll.h)
description: The same as InstallPKCS7Blob except that it returns the number of certificates actually installed in local stores.
helpviewer_keywords: ["IEnroll4 interface [Security]","InstallPKCS7BlobEx method","IEnroll4.InstallPKCS7BlobEx","IEnroll4::InstallPKCS7BlobEx","InstallPKCS7BlobEx","InstallPKCS7BlobEx method [Security]","InstallPKCS7BlobEx method [Security]","IEnroll4 interface","security.ienroll4_installpkcs7blobex","xenroll/IEnroll4::InstallPKCS7BlobEx"]
old-location: security\ienroll4_installpkcs7blobex.htm
tech.root: security
ms.assetid: 6a65eac6-3fe5-4464-876d-80eedaca7ae6
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],InstallPKCS7BlobEx method, IEnroll4.InstallPKCS7BlobEx, IEnroll4::InstallPKCS7BlobEx, InstallPKCS7BlobEx, InstallPKCS7BlobEx method [Security], InstallPKCS7BlobEx method [Security],IEnroll4 interface, security.ienroll4_installpkcs7blobex, xenroll/IEnroll4::InstallPKCS7BlobEx
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
 - IEnroll4::InstallPKCS7BlobEx
 - xenroll/IEnroll4::InstallPKCS7BlobEx
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
 - IEnroll4.InstallPKCS7BlobEx
---

# IEnroll4::InstallPKCS7BlobEx


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7BlobEx</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="/windows/desktop/SecGloss/c-gly">certificate stores</a>. The <b>InstallPKCS7BlobEx</b> method is the same as 
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob">InstallPKCS7Blob</a> except that it returns the number of certificates actually installed in local stores.

## -parameters

### -param pBlobPKCS7 [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains a certificate or chain of certificates.

### -param plCertInstalled [out]

Returns the number of certificates installed into local stores.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>