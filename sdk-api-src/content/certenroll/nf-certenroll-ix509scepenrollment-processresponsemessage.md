---
UID: NF:certenroll.IX509SCEPEnrollment.ProcessResponseMessage
title: IX509SCEPEnrollment::ProcessResponseMessage (certenroll.h)
description: Process a response message and return the disposition of the message.
helpviewer_keywords: ["IX509SCEPEnrollment interface [Security]","ProcessResponseMessage method","IX509SCEPEnrollment.ProcessResponseMessage","IX509SCEPEnrollment::ProcessResponseMessage","ProcessResponseMessage","ProcessResponseMessage method [Security]","ProcessResponseMessage method [Security]","IX509SCEPEnrollment interface","certenroll/IX509SCEPEnrollment::ProcessResponseMessage","security.ix509scepenrollment_processresponsemessage"]
old-location: security\ix509scepenrollment_processresponsemessage.htm
tech.root: security
ms.assetid: 4254fdf3-473f-4f22-a08f-13481fd9f779
ms.date: 12/05/2018
ms.keywords: IX509SCEPEnrollment interface [Security],ProcessResponseMessage method, IX509SCEPEnrollment.ProcessResponseMessage, IX509SCEPEnrollment::ProcessResponseMessage, ProcessResponseMessage, ProcessResponseMessage method [Security], ProcessResponseMessage method [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::ProcessResponseMessage, security.ix509scepenrollment_processresponsemessage
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
 - IX509SCEPEnrollment::ProcessResponseMessage
 - certenroll/IX509SCEPEnrollment::ProcessResponseMessage
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
 - IX509SCEPEnrollment.ProcessResponseMessage
---

# IX509SCEPEnrollment::ProcessResponseMessage


## -description

Process a response message and return the disposition of the message.

## -parameters

### -param strResponse [in]

### -param Encoding [in]

### -param pDisposition [out, retval]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initialize">Initialize</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage">CreateRequestMessage</a> methods or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initializeforpending">InitializeForPending</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>