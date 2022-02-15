---
UID: NF:certpol.INDESPolicy.Notify
title: INDESPolicy::Notify (certpol.h)
description: Notifies the plug-in of the transaction status of the SCEP certificate request.
helpviewer_keywords: ["INDESPolicy interface [Security]","Notify method","INDESPolicy.Notify","INDESPolicy::Notify","Notify","Notify method [Security]","Notify method [Security]","INDESPolicy interface","certpol/INDESPolicy::Notify","security.indespolicy_notify"]
old-location: security\indespolicy_notify.htm
tech.root: security
ms.assetid: dcb1c006-c709-4879-a9bf-8d441d26db8d
ms.date: 12/05/2018
ms.keywords: INDESPolicy interface [Security],Notify method, INDESPolicy.Notify, INDESPolicy::Notify, Notify, Notify method [Security], Notify method [Security],INDESPolicy interface, certpol/INDESPolicy::Notify, security.indespolicy_notify
req.header: certpol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certpol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INDESPolicy::Notify
 - certpol/INDESPolicy::Notify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - certpol.h
api_name:
 - INDESPolicy.Notify
---

# INDESPolicy::Notify


## -description

Notifies the plug-in of the transaction status of the SCEP certificate request.

## -parameters

### -param pwszChallenge [in]

The authentication and authorization SCEP challenge password for the user.

### -param pwszTransactionId [in]

The SCEP request transaction ID.

### -param disposition [in]

The disposition of the transaction.

### -param lastHResult [in]

The <b>HRESULT</b> of the last operation.

### -param pctbIssuedCertEncoded [in]

The requested certificate, if issued.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certpol/nn-certpol-indespolicy">INDESPolicy</a>