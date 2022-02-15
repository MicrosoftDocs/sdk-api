---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRetrieveCertificateMessage
title: IX509SCEPEnrollment::CreateRetrieveCertificateMessage (certenroll.h)
description: Retrieve a previously issued certificate.
helpviewer_keywords: ["CreateRetrieveCertificateMessage","CreateRetrieveCertificateMessage method [Security]","CreateRetrieveCertificateMessage method [Security]","IX509SCEPEnrollment interface","IX509SCEPEnrollment interface [Security]","CreateRetrieveCertificateMessage method","IX509SCEPEnrollment.CreateRetrieveCertificateMessage","IX509SCEPEnrollment::CreateRetrieveCertificateMessage","certenroll/IX509SCEPEnrollment::CreateRetrieveCertificateMessage","security.ix509scepenrollment_createretrievecertificatemessage"]
old-location: security\ix509scepenrollment_createretrievecertificatemessage.htm
tech.root: security
ms.assetid: 238a837f-4464-49ce-b87a-03abcfc0abea
ms.date: 12/05/2018
ms.keywords: CreateRetrieveCertificateMessage, CreateRetrieveCertificateMessage method [Security], CreateRetrieveCertificateMessage method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],CreateRetrieveCertificateMessage method, IX509SCEPEnrollment.CreateRetrieveCertificateMessage, IX509SCEPEnrollment::CreateRetrieveCertificateMessage, certenroll/IX509SCEPEnrollment::CreateRetrieveCertificateMessage, security.ix509scepenrollment_createretrievecertificatemessage
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509SCEPEnrollment::CreateRetrieveCertificateMessage
 - certenroll/IX509SCEPEnrollment::CreateRetrieveCertificateMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.CreateRetrieveCertificateMessage
---

# IX509SCEPEnrollment::CreateRetrieveCertificateMessage


## -description

Retrieve a previously issued certificate.

## -parameters

### -param Context [in]

### -param strIssuer [in]

ASN.1 encoded issuer name.

### -param IssuerEncoding [in]

### -param strSerialNumber [in]

### -param SerialNumberEncoding [in]

### -param Encoding [in]

### -param pValue [out, retval]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initializeforpending">InitializeForPending</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>