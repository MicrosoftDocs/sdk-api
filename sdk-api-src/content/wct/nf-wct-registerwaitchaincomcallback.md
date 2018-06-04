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

# RegisterWaitChainCOMCallback function


## -description


Register COM callback functions for WCT.


## -parameters




### -param CallStateCallback [in]

The address of the <b>CoGetCallState</b> function.


### -param ActivationStateCallback [in]

The address of the <b>CoGetActivationState</b> function.


## -returns



This function does not return a value.




## -remarks



If a thread is blocked on a COM call, WCT can retrieve COM ownership information using these callback functions. If this function is callback multiple times, only the last addresses retrieved are used.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7c5fa606-6e9b-41da-bfa9-1f066449d813">Using WCT</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d266a663-b101-4936-9574-f6ce223419ae">Wait Chain Traversal</a>
 

 

