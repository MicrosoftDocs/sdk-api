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

# IMSVidAnalogTuner::ChannelAvailable


## -description


The <b>ChannelAvailable</b> method queries whether a specified channel is available for viewing.

This method is currently not supported.


## -parameters




### -param nChannel [in]

Integer containing the channel.


### -param SignalStrength




### -param fSignalPresent






#### - pSignalStrength [in, out]

Pointer to a <b>long</b> value that specifies the signal strength.


#### - pfSignalPresent [out]

Receives a <b>VARIANT_BOOL</b> that indicates whether a signal is present.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/64a89038-4df1-4e30-8952-6dc039a2e18b">IAMTuner::SignalPresent</a>



<a href="https://msdn.microsoft.com/640143d3-6712-4e92-a1d9-0689637b3d90">IMSVidAnalogTuner Interface</a>
 

 

