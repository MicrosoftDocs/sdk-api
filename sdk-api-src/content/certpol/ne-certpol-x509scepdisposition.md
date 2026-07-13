---
UID: NE:certpol.X509SCEPDisposition
title: X509SCEPDisposition (certpol.h)
description: Describes the resulting disposition of a request to process a response message.
helpviewer_keywords: ["SCEPDispositionFailure","SCEPDispositionPending","SCEPDispositionSuccess","X509SCEPDisposition","X509SCEPDisposition enumeration [Security]","certpol/SCEPDispositionFailure","certpol/SCEPDispositionPending","certpol/SCEPDispositionSuccess","certpol/X509SCEPDisposition","security.x509scepdisposition"]
old-location: security\x509scepdisposition.htm
tech.root: security
ms.assetid: 635AAD37-261F-4F38-AD00-B3E8A5C55ABF
ms.date: 12/05/2018
ms.keywords: SCEPDispositionFailure, SCEPDispositionPending, SCEPDispositionSuccess, X509SCEPDisposition, X509SCEPDisposition enumeration [Security], certpol/SCEPDispositionFailure, certpol/SCEPDispositionPending, certpol/SCEPDispositionSuccess, certpol/X509SCEPDisposition, security.x509scepdisposition
req.header: certpol.h
req.include-header: CertEnroll.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: X509SCEPDisposition
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509SCEPDisposition
 - certpol/X509SCEPDisposition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - certpol.h
api_name:
 - X509SCEPDisposition
---

# X509SCEPDisposition enumeration


## -description

The <b>X509SCEPDisposition</b> enumeration   describes the resulting disposition of a request to process a response message. This enumeration is used by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509scepenrollment">IX509SCEPEnrollment</a> interface.

## -enum-fields

### -field SCEPDispositionUnknown:-1

### -field SCEPDispositionSuccess:0

The request was successful.

### -field SCEPDispositionFailure:2

The request failed.

### -field SCEPDispositionPending:3

The request has not completed yet.

### -field SCEPDispositionPendingChallenge:11

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage">ProcessResponseMessage</a>
