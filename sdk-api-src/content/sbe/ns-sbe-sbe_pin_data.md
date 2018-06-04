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

# SBE_PIN_DATA structure


## -description



This topic applies to Windows XP Service Pack 2 only.
          

The <b>STREAMBUFFER_ATTRIBUTE</b> structure contains performance data for the stream buffer filters.




## -struct-fields




### -field cDataBytes

Total sample payload, in bytes.


### -field cSamplesProcessed

Number of samples processed.


### -field cDiscontinuities

Number of discontinuities. See <a href="https://msdn.microsoft.com/57041c71-4c7e-463a-92f5-c77a76aa545a">IMediaSample::SetDiscontinuity</a>.


### -field cSyncPoints

Number of synchronization points. See <a href="https://msdn.microsoft.com/b2770045-c18b-4dbc-b104-873e07c0b5aa">IMediaSample::SetSyncPoint</a>.


### -field cTimestamps

Number of time stamps.


## -see-also




<a href="https://msdn.microsoft.com/15895ff3-37e5-4f89-bcce-3b9f060c0746">IStreamBufferDataCounters::GetData</a>



<a href="https://msdn.microsoft.com/90ac310a-7fd3-440f-9cf7-7d6eb58996cc">Stream Buffer Engine Structures</a>
 

 

