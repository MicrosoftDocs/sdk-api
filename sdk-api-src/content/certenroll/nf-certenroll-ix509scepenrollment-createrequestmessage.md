---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRequestMessage
title: IX509SCEPEnrollment::CreateRequestMessage (certenroll.h)
description: Create a PKCS10 request message with a challenge password. The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.
helpviewer_keywords: ["CreateRequestMessage","CreateRequestMessage method [Security]","CreateRequestMessage method [Security]","IX509SCEPEnrollment interface","IX509SCEPEnrollment interface [Security]","CreateRequestMessage method","IX509SCEPEnrollment.CreateRequestMessage","IX509SCEPEnrollment::CreateRequestMessage","certenroll/IX509SCEPEnrollment::CreateRequestMessage","security.ix509scepenrollment_createrequestmessage"]
old-location: security\ix509scepenrollment_createrequestmessage.htm
tech.root: security
ms.assetid: b86d6dc3-aa96-45f3-9551-f24c39ea6cbf
ms.date: 12/05/2018
ms.keywords: CreateRequestMessage, CreateRequestMessage method [Security], CreateRequestMessage method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],CreateRequestMessage method, IX509SCEPEnrollment.CreateRequestMessage, IX509SCEPEnrollment::CreateRequestMessage, certenroll/IX509SCEPEnrollment::CreateRequestMessage, security.ix509scepenrollment_createrequestmessage
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
 - IX509SCEPEnrollment::CreateRequestMessage
 - certenroll/IX509SCEPEnrollment::CreateRequestMessage
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
 - IX509SCEPEnrollment.CreateRequestMessage
---

# IX509SCEPEnrollment::CreateRequestMessage


## -description

Create a PKCS10 request message with a challenge password. The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.

## -parameters

### -param Encoding [in]

### -param pValue [out, retval]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-initialize">Initialize</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a>