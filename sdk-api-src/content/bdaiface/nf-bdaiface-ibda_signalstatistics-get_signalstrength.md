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

# IBDA_SignalStatistics::get_SignalStrength


## -description



The <b>get_SignalStrength</b> method retrieves a value that indicates the strength of the signal in decibels.




## -parameters




### -param plDbStrength [out]

Pointer that receives the signal strength value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ee8b25d5-d39b-42ac-9f6a-0825e396241c">IBDA_SignalStatistics Interface</a>



<a href="https://msdn.microsoft.com/3a1f11b7-09f4-430a-8976-81f15ea22b1a">IBDA_SignalStatistics::put_SignalStrength</a>
 

 

