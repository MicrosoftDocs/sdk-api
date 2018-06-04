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

# _RM_SEND_WINDOW structure


## -description


The <b>RM_SEND_WINDOW</b> structure specifies the Reliable Multicast send window. This structure is used with the <a href="https://msdn.microsoft.com/cb99960e-428b-4ef1-a6a5-e4bdb497c771">RM_RATE_WINDOW_SIZE</a> socket option.


## -struct-fields




### -field RateKbitsPerSec

Transmission rate for the send window, in kilobits per second.


### -field WindowSizeInMSecs

Window size for the send window, in milliseconds.


### -field WindowSizeInBytes

Window size for the session, in bytes.


## -remarks



Any combination of the three available members may be set for a given socket option call. For example, one, any two, or all three members may be specified during a <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function call. Regardless of settings, Windows enforces the following ratio: <b>TransmissionRate</b> == (<b>WindowSizeBytes</b>/<b>WindowSizeMSecs</b>) * 8. As such, setting any two parameters effectively sets the third to ensure optimum performance. 

The combination of these members can affect the resources used on a PGM sender's computer. For example, a large transmission rate value combined with a large window size results in more required buffer space.




## -see-also




<a href="https://msdn.microsoft.com/cb99960e-428b-4ef1-a6a5-e4bdb497c771">IPPROTO_RM Socket Options</a>



<a href="https://msdn.microsoft.com/81c203ed-739f-4a06-99a1-9a99c6164edc">Reliable Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket Options</a>



<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>
 

 

