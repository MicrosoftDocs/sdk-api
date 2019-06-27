---
UID: NF:xenroll.IEnroll2.InstallPKCS7Blob
title: IEnroll2::InstallPKCS7Blob (xenroll.h)
author: windows-sdk-content
description: Processes a certificate or chain of certificates, placing them into the appropriate certificate stores. This method differs from the acceptPKCS7Blob method in that InstallPKCS7Blob does not receive a request certificate.
old-location: security\ienroll4_installpkcs7blob.htm
tech.root: SecCrypto
ms.assetid: fa704c5e-f6ec-4187-b787-7b15cc7d4eb4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll2 interface [Security],InstallPKCS7Blob method, IEnroll2.InstallPKCS7Blob, IEnroll2::InstallPKCS7Blob, InstallPKCS7Blob, InstallPKCS7Blob method [Security], InstallPKCS7Blob method [Security],IEnroll2 interface, security.ienroll4_installpkcs7blob, xenroll/IEnroll2::InstallPKCS7Blob
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll2.InstallPKCS7Blob"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll2.InstallPKCS7Blob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll2::InstallPKCS7Blob


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7Blob</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate stores</a>. This method differs from the  <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a> method in that  <b>InstallPKCS7Blob</b> does not receive a request certificate. This method was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.


## -parameters




### -param pBlobPKCS7 [in]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains a certificate or chain of certificates.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll2</a>
 

 

