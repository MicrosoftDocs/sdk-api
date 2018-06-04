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

# IMbnSignalEvents::OnSignalStateChange


## -description


This notification method is called by the Mobile Broadband service to indicate that a signal quality update is available.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/2b60d078-ccbd-4cc5-addf-e6e95832b3a1">IMbnSignal</a> interface  for which the signal quality update was received.


## -returns



This method must return <b>S_OK</b>.




## -remarks



<b>OnSignalStateChange</b> is called by the Mobile Broadband service to notify a calling application that a signal quality update is available.  This includes an update of the signal notification period, threshold for signal notification, signal strength received, and error rate in the received signal. 
An application can get updated values from the <a href="https://msdn.microsoft.com/2b60d078-ccbd-4cc5-addf-e6e95832b3a1">IMbnSignal</a> interface passed in this method.





## -see-also




<a href="https://msdn.microsoft.com/9e52168a-c6f9-4154-b8b9-8ae6cb771d46">IMbnSignalEvents</a>
 

 

