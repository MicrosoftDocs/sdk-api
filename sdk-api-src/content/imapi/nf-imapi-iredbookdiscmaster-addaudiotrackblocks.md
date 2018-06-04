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

# IRedbookDiscMaster::AddAudioTrackBlocks


## -description


Adds blocks of audio data to the currently open track. This method can be called repeatedly until there is no space available or the track is full.


## -parameters




### -param pby [in]

Pointer to an array of track blocks. The format is 44.1 KHz 16-bit stereo RAW audio samples, in the same format as used by WAV in the data section.


### -param cb [in]

Size of the array, in bytes. This count must be a multiple of the audio block size.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



After all blocks are added, call the 
<a href="https://msdn.microsoft.com/01ec0eba-d592-46eb-8029-86cb678b8b34">CloseAudioTrack</a> method to finish the track.

If a call to this method would overrun the number of available audio blocks, then the method will return IMAPI_E_DISCFULL and keep as much of the audio data as it can. In contrast, the 
<a href="https://msdn.microsoft.com/91517103-71c5-450c-9d93-584f94cd2c45">IJolietDiscMaster::AddData</a> method does not keep any of the data, so there are no bad files.




## -see-also




<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>
 

 

