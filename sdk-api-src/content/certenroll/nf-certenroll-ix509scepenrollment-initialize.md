---
UID: NF:certenroll.IX509SCEPEnrollment.Initialize
title: IX509SCEPEnrollment::Initialize (certenroll.h)
description: Initialize the instance in preparation for a new request.
helpviewer_keywords: ["IX509SCEPEnrollment interface [Security]","Initialize method","IX509SCEPEnrollment.Initialize","IX509SCEPEnrollment::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","IX509SCEPEnrollment interface","certenroll/IX509SCEPEnrollment::Initialize","security.ix509scepenrollment_initialize"]
old-location: security\ix509scepenrollment_initialize.htm
tech.root: security
ms.assetid: dcb887ab-c8b7-42e7-8b49-93755d24ba70
ms.date: 12/05/2018
ms.keywords: IX509SCEPEnrollment interface [Security],Initialize method, IX509SCEPEnrollment.Initialize, IX509SCEPEnrollment::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::Initialize, security.ix509scepenrollment_initialize
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
 - IX509SCEPEnrollment::Initialize
 - certenroll/IX509SCEPEnrollment::Initialize
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
 - IX509SCEPEnrollment.Initialize
---

# IX509SCEPEnrollment::Initialize


## -description

Initialize the instance in preparation for a new request.

## -parameters

### -param pRequest [in]

An instance of a request that has already been initialized.

### -param strThumbprint [in]

The CA certificate thumbprint.

### -param ThumprintEncoding [in]

The encoding of the CA certificate thumbprint.

### -param strServerCertificates [in]

A PKCS7 request with CA and SCEP RA certificates.

### -param Encoding [in]

The encoding type of the request.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method expects an SCEP server signature EA certificate and an SCEP server encryption EA certificate, both signed by the CA certificate.

This method fails if any of the expected certificates is missing, or if the thumbprint doesn't match the CA certificate.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>