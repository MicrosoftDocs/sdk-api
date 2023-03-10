---
UID: NF:certenroll.IX509SCEPEnrollment.put_SignerCertificate
title: IX509SCEPEnrollment::put_SignerCertificate (certenroll.h)
description: Gets or sets the signer certificate for the request. (Put)
helpviewer_keywords: ["IX509SCEPEnrollment interface [Security]","SignerCertificate property","IX509SCEPEnrollment.SignerCertificate","IX509SCEPEnrollment.put_SignerCertificate","IX509SCEPEnrollment::SignerCertificate","IX509SCEPEnrollment::get_SignerCertificate","IX509SCEPEnrollment::put_SignerCertificate","SignerCertificate property [Security]","SignerCertificate property [Security]","IX509SCEPEnrollment interface","certenroll/IX509SCEPEnrollment::SignerCertificate","certenroll/IX509SCEPEnrollment::get_SignerCertificate","certenroll/IX509SCEPEnrollment::put_SignerCertificate","put_SignerCertificate","security.ix509scepenrollment_signercertificate"]
old-location: security\ix509scepenrollment_signercertificate.htm
tech.root: security
ms.assetid: 7d01acc5-158d-4429-a2e8-d179571f9a1c
ms.date: 12/05/2018
ms.keywords: IX509SCEPEnrollment interface [Security],SignerCertificate property, IX509SCEPEnrollment.SignerCertificate, IX509SCEPEnrollment.put_SignerCertificate, IX509SCEPEnrollment::SignerCertificate, IX509SCEPEnrollment::get_SignerCertificate, IX509SCEPEnrollment::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::SignerCertificate, certenroll/IX509SCEPEnrollment::get_SignerCertificate, certenroll/IX509SCEPEnrollment::put_SignerCertificate, put_SignerCertificate, security.ix509scepenrollment_signercertificate
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
 - IX509SCEPEnrollment::put_SignerCertificate
 - certenroll/IX509SCEPEnrollment::put_SignerCertificate
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
 - IX509SCEPEnrollment.SignerCertificate
 - IX509SCEPEnrollment.get_SignerCertificate
 - IX509SCEPEnrollment.put_SignerCertificate
---

# IX509SCEPEnrollment::put_SignerCertificate


## -description

Gets or sets the signer certificate for the request.

This property is read/write.

## -parameters

## -remarks

To create a renewal request, you must set this property prior to calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage">CreateRequestMessage</a> method. Otherwise, the <b>CreateRequestMessage</b> method will create a new request and generate a self-signed certificate using the same private key as the inner PKCSV10 reqeust.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>
