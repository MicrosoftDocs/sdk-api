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

# IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 callback function


## -description


The <b>IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</b> function indicates whether the Trusted Intermediary Agent (TIA) will dictate the keys for the SA being negotiated.


## -parameters




### -param *ikeTraffic [in]

Type: <b>const <a href="https://msdn.microsoft.com/99cb3774-7afd-44fd-9c3e-e2d913aaeecb">IKEEXT_TRAFFIC0</a>*</b>

Specifies the traffic for which keys should be set or retrieved.


### -param *willDictateKey [out]

Type: <b>BOOL*</b>

True if the TIA will dictate the keys; otherwise, false.


### -param *weight [out]

Type: <b>UINT32*</b>

Specifies the weight that this TIA should be given compared to any peers.


## -returns



This function pointer does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister</a> to register this function pointer.

If the TIA wants to dictate the keys, and its weight is higher than that of any peers, IPsec will subsequently call <a href="https://msdn.microsoft.com/A69E44FF-A58D-426B-BD59-8EB4B5A63B66">IPSEC_KEY_MANAGER_DICTATE_KEY0</a>.




## -see-also




<a href="https://msdn.microsoft.com/99cb3774-7afd-44fd-9c3e-e2d913aaeecb">IKEEXT_TRAFFIC0</a>



<a href="https://msdn.microsoft.com/A69E44FF-A58D-426B-BD59-8EB4B5A63B66">IPSEC_KEY_MANAGER_DICTATE_KEY0</a>



<a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

