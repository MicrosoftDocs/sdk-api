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

# _HTTP_FLOWRATE_INFO structure


## -description


The transfer rate of a response


## -struct-fields




### -field Flags

An <a href="https://msdn.microsoft.com/cafa3b04-ac8b-4269-bfa9-fe8e9ab65936">HTTP_PROPERTY_FLAGS</a> structure specifying whether the property is present.


### -field MaxBandwidth

The maximum bandwidth represented in bytes/second.  This is the maximum bandwidth for the response after the burst content, whose size is specified in <b>BurstSize</b>,  has been sent.


### -field MaxPeakBandwidth

The peak bandwidth represented in bytes/second.  This is the maximum bandwidth at which the burst is delivered.


### -field BurstSize

The size of the content, in bytes, to be delivered at <b>MaxPeakBandwidth</b>.  Once this content has been delivered, the response is throttled at <b>MaxBandwidth</b>.  If the HTTP Server application sends responses at a rate slower than <b>MaxBandwidth</b>, the response is subject to burst again at <b>MaxPeakBandwidth</b> to maximize bandwidth utilization. 


## -remarks



This structure allows an HTTP Server application to maximize the network bandwidth use by throttling down the transfer rate of an HTTP response.  This is especially useful in serving media content where the initial burst of the content is served at a higher transfer rate and then throttled.  This allows content from a larger number of media to be served concurrently.

The transfer rate is allowed to exceed <b> MaxBandwidth</b> in two cases:<ul>
<li>If the connection slows and the transfer rate falls below <b> MaxBandwidth</b>, the application can go beyond <b> MaxBandwidth</b> to catch up.</li>
<li>The beginning of a response is allowed to exceed <b> MaxBandwidth</b>.  For example, a server may  transfer media file at high speed at the beginning in order to expedite playback on the client.
For example, if that client needs initial 20KB of the file to start playback, the server might have this variable set to 20KB.
</li>
</ul>When <b> MaxBandwidth</b> is exceeded, <b> MaxPeakBandwidth </b> is still the absolute upper limit.  
 




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>
 

 

