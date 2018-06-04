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

# _MFBYTESTREAM_BUFFERING_PARAMS structure


## -description



Specifies the buffering parameters for a network byte stream.




## -struct-fields




### -field cbTotalFileSize

Size of the file, in bytes. If the total size is unknown, set this member to -1.


### -field cbPlayableDataSize

Size of the playable media data in the file, excluding any trailing data that is not useful for playback. If this value is unknown, set this member to -1.


### -field prgBuckets

Pointer to an array of <a href="https://msdn.microsoft.com/aa95a8f0-2f4c-4d7e-81c3-8a14a6ffa54e">MF_LEAKY_BUCKET_PAIR</a> structures. Each member of the array gives the buffer window for a particular bit rate.


### -field cBuckets

The number of elements in the <b>prgBuckets</b> array.


### -field qwNetBufferingTime

Amount of data to buffer from the network, in 100-nanosecond units. This value is in addition to the buffer windows defined in the <b>prgBuckets</b> member.


### -field qwExtraBufferingTimeDuringSeek

Amount of additional data to buffer when seeking, in 100-nanosecond units. This value reflects the fact that downloading must start from the previous key frame before the seek point. If the value is unknown, set this member to zero.


### -field qwPlayDuration

The playback duration of the file, in 100-nanosecond units. If the duration is unknown, set this member to zero.


### -field dRate

Playback rate.


## -see-also




<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

