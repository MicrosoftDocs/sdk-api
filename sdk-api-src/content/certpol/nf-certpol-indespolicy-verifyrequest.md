---
UID: NF:certpol.INDESPolicy.VerifyRequest
title: INDESPolicy::VerifyRequest (certpol.h)
description: Verifies the NDES certificate request for submission to the CA.
helpviewer_keywords: ["INDESPolicy interface [Security]","VerifyRequest method","INDESPolicy.VerifyRequest","INDESPolicy::VerifyRequest","VerifyRequest","VerifyRequest method [Security]","VerifyRequest method [Security]","INDESPolicy interface","certpol/INDESPolicy::VerifyRequest","security.indespolicy_verifyrequest"]
old-location: security\indespolicy_verifyrequest.htm
tech.root: security
ms.assetid: 420ef521-07ff-466c-a3c2-cbffd896ca16
ms.date: 12/05/2018
ms.keywords: INDESPolicy interface [Security],VerifyRequest method, INDESPolicy.VerifyRequest, INDESPolicy::VerifyRequest, VerifyRequest, VerifyRequest method [Security], VerifyRequest method [Security],INDESPolicy interface, certpol/INDESPolicy::VerifyRequest, security.indespolicy_verifyrequest
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
 - INDESPolicy::VerifyRequest
 - certpol/INDESPolicy::VerifyRequest
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
 - INDESPolicy.VerifyRequest
---

# INDESPolicy::VerifyRequest


## -description

Verifies the NDES certificate request for submission to the CA.

## -parameters

### -param pctbRequest [in]

The encoded PKCS#10 request.

### -param pctbSigningCertEncoded [in]

The valid signing certificate for a renewal request.

### -param pwszTemplate [in]

The template being requested for, as determined by NDES.

### -param pwszTransactionId [in]

The SCEP request transaction ID.

### -param pfVerified [out, retval]

True if the challenge is verified; otherwise false.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certpol/nn-certpol-indespolicy">INDESPolicy</a>