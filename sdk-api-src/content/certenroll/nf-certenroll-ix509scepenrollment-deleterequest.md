---
UID: NF:certenroll.IX509SCEPEnrollment.DeleteRequest
title: IX509SCEPEnrollment::DeleteRequest (certenroll.h)
description: Delete any certificates or keys created for the request.
helpviewer_keywords: ["DeleteRequest","DeleteRequest method [Security]","DeleteRequest method [Security]","IX509SCEPEnrollment interface","IX509SCEPEnrollment interface [Security]","DeleteRequest method","IX509SCEPEnrollment.DeleteRequest","IX509SCEPEnrollment::DeleteRequest","certenroll/IX509SCEPEnrollment::DeleteRequest","security.ix509scepenrollment_deleterequest"]
old-location: security\ix509scepenrollment_deleterequest.htm
tech.root: security
ms.assetid: d709dd46-b6ed-4471-a601-e140a139f57e
ms.date: 12/05/2018
ms.keywords: DeleteRequest, DeleteRequest method [Security], DeleteRequest method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],DeleteRequest method, IX509SCEPEnrollment.DeleteRequest, IX509SCEPEnrollment::DeleteRequest, certenroll/IX509SCEPEnrollment::DeleteRequest, security.ix509scepenrollment_deleterequest
f1_keywords:
- certenroll/IX509SCEPEnrollment.DeleteRequest
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Certenroll.dll
api_name:
- IX509SCEPEnrollment.DeleteRequest
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509SCEPEnrollment::DeleteRequest


## -description


Delete any certificates or keys created for the request.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must set the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-get_transactionid">TransactionId</a> property and call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initializeforpending">InitializeForPending</a> method before calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>
 

 

