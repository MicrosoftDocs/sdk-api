---
UID: NF:certenroll.IX509SCEPEnrollment.put_ServerCapabilities
title: IX509SCEPEnrollment::put_ServerCapabilities (certenroll.h)
description: Sets the preferred hash and encryption algorithms for the request.
helpviewer_keywords: ["IX509SCEPEnrollment interface [Security]","ServerCapabilities property","IX509SCEPEnrollment.ServerCapabilities","IX509SCEPEnrollment.put_ServerCapabilities","IX509SCEPEnrollment::ServerCapabilities","IX509SCEPEnrollment::put_ServerCapabilities","ServerCapabilities property [Security]","ServerCapabilities property [Security]","IX509SCEPEnrollment interface","certenroll/IX509SCEPEnrollment::ServerCapabilities","certenroll/IX509SCEPEnrollment::put_ServerCapabilities","put_ServerCapabilities","security.ix509scepenrollment_servercapabilities"]
old-location: security\ix509scepenrollment_servercapabilities.htm
tech.root: security
ms.assetid: fcfed23f-7798-4b56-afcd-65975a2d39bd
ms.date: 12/05/2018
ms.keywords: IX509SCEPEnrollment interface [Security],ServerCapabilities property, IX509SCEPEnrollment.ServerCapabilities, IX509SCEPEnrollment.put_ServerCapabilities, IX509SCEPEnrollment::ServerCapabilities, IX509SCEPEnrollment::put_ServerCapabilities, ServerCapabilities property [Security], ServerCapabilities property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::ServerCapabilities, certenroll/IX509SCEPEnrollment::put_ServerCapabilities, put_ServerCapabilities, security.ix509scepenrollment_servercapabilities
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
 - IX509SCEPEnrollment::put_ServerCapabilities
 - certenroll/IX509SCEPEnrollment::put_ServerCapabilities
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
 - IX509SCEPEnrollment.ServerCapabilities
 - IX509SCEPEnrollment.put_ServerCapabilities
---

# IX509SCEPEnrollment::put_ServerCapabilities


## -description

Sets the preferred hash and encryption algorithms for the request.

This property is write-only.

## -parameters

## -remarks

If you do not set this property, then the default hash and encryption algorithms will be used.

This property must be set before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage">CreateRequestMessage</a>, <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage">CreateRetrievePendingMessage</a>, or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage">CreateRetrieveCertificateMessage</a> methods.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>