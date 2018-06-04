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

# tagTimedLevel structure


## -description


The <b>TimedLevel</b> structure holds data returned from the spectrum filter.


## -struct-fields




### -field frequency

A stereo snapshot of the frequency spectrum of the audio data at a time specified by the Plug-in Manager. It can be used for frequency spectrum effects such as real-time analyzers. The frequency value of the first cell is 20 Hz, and the frequency value of the last cell is 22050 Hz.


### -field waveform

A stereo snapshot of the power value of the audio data at a time specified by the Plug-in Manager as the first element; the next 1024 stereo power values fill out the rest of the array. It can be used for oscilloscope-type effects.


### -field state

One member of the <a href="https://msdn.microsoft.com/7cd17639-e491-4066-838a-236554733874">PlayerState</a> enumeration type.


### -field timeStamp

The time the snapshot took place, in a 64-bit integer. The time value is provided in 100-nanosecond units.


## -remarks



The array dimension <b>SA_BUFFER_SIZE</b> is currently 1024.

The first dimension of each array corresponds to the channel: 0 is a monaural signal or the left channel of a stereo signal, and 1 is the right channel of a stereo signal. If the signal is monaural, the values in the array that would correspond to the right channel are undefined.

The second dimension contains the sampled levels. The frequency data ranges from 0 to 255. The waveform data represents -128 to 127 but is stored as 0 to 255, so subtract 128 to get the correct value.




## -see-also




<a href="https://msdn.microsoft.com/7cd17639-e491-4066-838a-236554733874">PlayerState</a>



<a href="https://msdn.microsoft.com/b54238a6-3d17-47b8-b650-bbe3473064da">Visualization Structures and Enumeration Types</a>
 

 

