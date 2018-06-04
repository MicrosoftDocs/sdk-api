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

# _DMO_OUTPUT_DATA_BUFFER_FLAGS enumeration


## -description



The <b>DMO_OUTPUT_DATA_BUFFER_FLAGS</b> enumeration defines flags that describe an output buffer.




## -enum-fields




### -field DMO_OUTPUT_DATA_BUFFERF_SYNCPOINT


            The beginning of the data is a synchronization point.
          A <i>synchronization point</i> is a random access point. For encoded video, this a sample that can be used as a decoding start point (key frame). For uncompressed audio or video, every sample is a synchronization point.


### -field DMO_OUTPUT_DATA_BUFFERF_TIME

The buffer's time stamp is valid.


            The buffer's indicated time length is valid.
          


### -field DMO_OUTPUT_DATA_BUFFERF_TIMELENGTH


            The buffer's indicated time length is valid.
          


### -field DMO_OUTPUT_DATA_BUFFERF_DISCONTINUITY


### -field DMO_OUTPUT_DATA_BUFFERF_INCOMPLETE


            There is still input data available for processing, but the output buffer is full.
          


## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a>
 

 

