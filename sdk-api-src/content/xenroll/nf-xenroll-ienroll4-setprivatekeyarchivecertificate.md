---
UID: NF:xenroll.IEnroll4.SetPrivateKeyArchiveCertificate
title: IEnroll4::SetPrivateKeyArchiveCertificate (xenroll.h)
description: The SetPrivateKeyArchiveCertificate method specifies the certificate used to archive the private key. This method was first defined in the IEnroll4 interface.
helpviewer_keywords: ["IEnroll4 interface [Security]","SetPrivateKeyArchiveCertificate method","IEnroll4.SetPrivateKeyArchiveCertificate","IEnroll4::SetPrivateKeyArchiveCertificate","SetPrivateKeyArchiveCertificate","SetPrivateKeyArchiveCertificate method [Security]","SetPrivateKeyArchiveCertificate method [Security]","IEnroll4 interface","security.ienroll4_setprivatekeyarchivecertificate","xenroll/IEnroll4::SetPrivateKeyArchiveCertificate"]
old-location: security\ienroll4_setprivatekeyarchivecertificate.htm
tech.root: security
ms.assetid: e37a8055-4074-425b-8f88-69b898855824
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],SetPrivateKeyArchiveCertificate method, IEnroll4.SetPrivateKeyArchiveCertificate, IEnroll4::SetPrivateKeyArchiveCertificate, SetPrivateKeyArchiveCertificate, SetPrivateKeyArchiveCertificate method [Security], SetPrivateKeyArchiveCertificate method [Security],IEnroll4 interface, security.ienroll4_setprivatekeyarchivecertificate, xenroll/IEnroll4::SetPrivateKeyArchiveCertificate
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
 - IEnroll4::SetPrivateKeyArchiveCertificate
 - xenroll/IEnroll4::SetPrivateKeyArchiveCertificate
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
 - IEnroll4.SetPrivateKeyArchiveCertificate
---

# IEnroll4::SetPrivateKeyArchiveCertificate


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SetPrivateKeyArchiveCertificate</b> method specifies the certificate used to archive the private key. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param pPrivateKeyArchiveCert [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that specifies the certificate used to archive the private key.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>