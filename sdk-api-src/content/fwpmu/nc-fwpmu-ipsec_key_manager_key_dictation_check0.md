---
UID: NC:fwpmu.IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
title: IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
author: windows-sdk-content
description: Indicates whether the Trusted Intermediary Agent (TIA) will dictate the keys for the SA being negotiated.
old-location: fwp\ipsec_key_manager_key_dictation_check0.htm
tech.root: fwp
ms.assetid: 0B91B57C-6943-4702-8926-8ED2B7B3E48D
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0, IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 function, IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0 function pointer [Filtering], fwp.ipsec_key_manager_key_dictation_check0, fwpmu/IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

