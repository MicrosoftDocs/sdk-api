---
UID: NF:certpol.INDESPolicy.GenerateChallenge
title: INDESPolicy::GenerateChallenge (certpol.h)
description: Performs the policy decision whether to issue a challenge password to the SCEP client.
helpviewer_keywords: ["GenerateChallenge","GenerateChallenge method [Security]","GenerateChallenge method [Security]","INDESPolicy interface","INDESPolicy interface [Security]","GenerateChallenge method","INDESPolicy.GenerateChallenge","INDESPolicy::GenerateChallenge","certpol/INDESPolicy::GenerateChallenge","security.indespolicy_generatechallenge"]
old-location: security\indespolicy_generatechallenge.htm
tech.root: security
ms.assetid: e09ef64c-5b4c-41ef-942a-1080cd566a5b
ms.date: 12/05/2018
ms.keywords: GenerateChallenge, GenerateChallenge method [Security], GenerateChallenge method [Security],INDESPolicy interface, INDESPolicy interface [Security],GenerateChallenge method, INDESPolicy.GenerateChallenge, INDESPolicy::GenerateChallenge, certpol/INDESPolicy::GenerateChallenge, security.indespolicy_generatechallenge
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
 - INDESPolicy::GenerateChallenge
 - certpol/INDESPolicy::GenerateChallenge
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
 - INDESPolicy.GenerateChallenge
---

# INDESPolicy::GenerateChallenge


## -description

Performs the policy decision whether to issue a challenge password to the SCEP client.

## -parameters

### -param pwszTemplate [in]

The template being requested for, as determined by NDES.

### -param pwszParams [in]

Parameters specific to the policy module implementation.

### -param ppwszResponse [out, retval]

After the user has been authenticated and authorized, the <i>ppwsxResponse</i> parameter contains the SCEP challenge password for the user. NDES will free this resource.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certpol/nn-certpol-indespolicy">INDESPolicy</a>