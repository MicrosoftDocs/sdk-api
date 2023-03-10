---
UID: NF:xenroll.IEnroll4.GetPrivateKeyArchiveCertificate
title: IEnroll4::GetPrivateKeyArchiveCertificate (xenroll.h)
description: The GetPrivateKeyArchiveCertificate method retrieves the certificate used to archive the private key. This method was first defined in the IEnroll4 interface.
helpviewer_keywords: ["GetPrivateKeyArchiveCertificate","GetPrivateKeyArchiveCertificate method [Security]","GetPrivateKeyArchiveCertificate method [Security]","IEnroll4 interface","IEnroll4 interface [Security]","GetPrivateKeyArchiveCertificate method","IEnroll4.GetPrivateKeyArchiveCertificate","IEnroll4::GetPrivateKeyArchiveCertificate","security.ienroll4_getprivatekeyarchivecertificate","xenroll/IEnroll4::GetPrivateKeyArchiveCertificate"]
old-location: security\ienroll4_getprivatekeyarchivecertificate.htm
tech.root: security
ms.assetid: 0fdcd4ff-2dd1-4654-9901-a9824d4eddec
ms.date: 12/05/2018
ms.keywords: GetPrivateKeyArchiveCertificate, GetPrivateKeyArchiveCertificate method [Security], GetPrivateKeyArchiveCertificate method [Security],IEnroll4 interface, IEnroll4 interface [Security],GetPrivateKeyArchiveCertificate method, IEnroll4.GetPrivateKeyArchiveCertificate, IEnroll4::GetPrivateKeyArchiveCertificate, security.ienroll4_getprivatekeyarchivecertificate, xenroll/IEnroll4::GetPrivateKeyArchiveCertificate
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
 - IEnroll4::GetPrivateKeyArchiveCertificate
 - xenroll/IEnroll4::GetPrivateKeyArchiveCertificate
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
 - IEnroll4.GetPrivateKeyArchiveCertificate
---

# IEnroll4::GetPrivateKeyArchiveCertificate


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetPrivateKeyArchiveCertificate</b> method retrieves the certificate used to archive the private key. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.



## -returns

Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that represents the certificate used to archive the private key, or <b>NULL</b> if an error is encountered.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
