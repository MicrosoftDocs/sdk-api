---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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




<a href="https://msdn.microsoft.com/9ed31493-832a-4f66-bb95-02ef1ad7ca15">INDESPolicy</a>
 

 

