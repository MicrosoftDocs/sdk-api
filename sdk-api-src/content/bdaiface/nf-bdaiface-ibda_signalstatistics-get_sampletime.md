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

# IBDA_SignalStatistics::get_SampleTime


## -description



The <b>get_SampleTime</b> method retrieves the sample time used to measure the signal.




## -parameters




### -param plmsSampleTime [out]

Pointer that receives the sample time.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ee8b25d5-d39b-42ac-9f6a-0825e396241c">IBDA_SignalStatistics Interface</a>



<a href="https://msdn.microsoft.com/086fd3ad-26d7-4b5b-b73a-a7d4db44d2c2">IBDA_SignalStatistics::put_SampleTime</a>
 

 

