---
UID: NF:certpol.INDESPolicy.VerifyRequest
title: INDESPolicy::VerifyRequest
author: windows-sdk-content
description: Verifies the NDES certificate request for submission to the CA.
old-location: security\indespolicy_verifyrequest.htm
tech.root: seccrypto
ms.assetid: 420ef521-07ff-466c-a3c2-cbffd896ca16
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: INDESPolicy interface [Security],VerifyRequest method, INDESPolicy.VerifyRequest, INDESPolicy::VerifyRequest, VerifyRequest, VerifyRequest method [Security], VerifyRequest method [Security],INDESPolicy interface, certpol/INDESPolicy::VerifyRequest, security.indespolicy_verifyrequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - certpol.h
api_name:
 - INDESPolicy.VerifyRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn383665(v=VS.85).aspx">INDESPolicy</a>
 

 

