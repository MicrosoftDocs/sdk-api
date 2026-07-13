---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRetrievePendingMessage
title: IX509SCEPEnrollment::CreateRetrievePendingMessage (certenroll.h)
description: Create a message for certificate polling (manual enrollment).
helpviewer_keywords: ["CreateRetrievePendingMessage","CreateRetrievePendingMessage method [Security]","CreateRetrievePendingMessage method [Security]","IX509SCEPEnrollment interface","IX509SCEPEnrollment interface [Security]","CreateRetrievePendingMessage method","IX509SCEPEnrollment.CreateRetrievePendingMessage","IX509SCEPEnrollment::CreateRetrievePendingMessage","certenroll/IX509SCEPEnrollment::CreateRetrievePendingMessage","security.ix509scepenrollment_createretrievependingmessage"]
old-location: security\ix509scepenrollment_createretrievependingmessage.htm
tech.root: security
ms.assetid: 86d031b0-2009-460b-8bed-fe7a0489f22b
ms.date: 12/05/2018
ms.keywords: CreateRetrievePendingMessage, CreateRetrievePendingMessage method [Security], CreateRetrievePendingMessage method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],CreateRetrievePendingMessage method, IX509SCEPEnrollment.CreateRetrievePendingMessage, IX509SCEPEnrollment::CreateRetrievePendingMessage, certenroll/IX509SCEPEnrollment::CreateRetrievePendingMessage, security.ix509scepenrollment_createretrievependingmessage
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
 - IX509SCEPEnrollment::CreateRetrievePendingMessage
 - certenroll/IX509SCEPEnrollment::CreateRetrievePendingMessage
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
 - IX509SCEPEnrollment.CreateRetrievePendingMessage
---

# IX509SCEPEnrollment::CreateRetrievePendingMessage


## -description

Create a message for certificate polling (manual enrollment).

## -parameters

### -param Encoding [in]

### -param pValue [out, retval]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initializeforpending">InitializeForPending</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>