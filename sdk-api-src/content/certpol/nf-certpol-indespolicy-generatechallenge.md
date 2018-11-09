---
UID: NF:certpol.INDESPolicy.GenerateChallenge
title: INDESPolicy::GenerateChallenge
author: windows-sdk-content
description: Performs the policy decision whether to issue a challenge password to the SCEP client.
old-location: security\indespolicy_generatechallenge.htm
tech.root: seccrypto
ms.assetid: e09ef64c-5b4c-41ef-942a-1080cd566a5b
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GenerateChallenge, GenerateChallenge method [Security], GenerateChallenge method [Security],INDESPolicy interface, INDESPolicy interface [Security],GenerateChallenge method, INDESPolicy.GenerateChallenge, INDESPolicy::GenerateChallenge, certpol/INDESPolicy::GenerateChallenge, security.indespolicy_generatechallenge
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
 - INDESPolicy.GenerateChallenge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn383665(v=VS.85).aspx">INDESPolicy</a>
 

 

