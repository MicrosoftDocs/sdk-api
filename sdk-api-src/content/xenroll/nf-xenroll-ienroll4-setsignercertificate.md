---
UID: NF:xenroll.IEnroll4.SetSignerCertificate
title: IEnroll4::SetSignerCertificate (xenroll.h)
description: The SetSignerCertificate method specifies the signer's certificate. This method was first defined in the IEnroll4 interface.
helpviewer_keywords: ["IEnroll4 interface [Security]","SetSignerCertificate method","IEnroll4.SetSignerCertificate","IEnroll4::SetSignerCertificate","SetSignerCertificate","SetSignerCertificate method [Security]","SetSignerCertificate method [Security]","IEnroll4 interface","security.ienroll4_setsignercertificate","xenroll/IEnroll4::SetSignerCertificate"]
old-location: security\ienroll4_setsignercertificate.htm
tech.root: security
ms.assetid: 1c970f6b-6b8f-4396-b59b-d6b58d52172b
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],SetSignerCertificate method, IEnroll4.SetSignerCertificate, IEnroll4::SetSignerCertificate, SetSignerCertificate, SetSignerCertificate method [Security], SetSignerCertificate method [Security],IEnroll4 interface, security.ienroll4_setsignercertificate, xenroll/IEnroll4::SetSignerCertificate
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
 - IEnroll4::SetSignerCertificate
 - xenroll/IEnroll4::SetSignerCertificate
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
 - IEnroll4.SetSignerCertificate
---

# IEnroll4::SetSignerCertificate


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetSignerCertificate</b> method specifies the signer's certificate. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param pSignerCert [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that represents the signer's certificate.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>