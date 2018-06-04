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

# _AUDCLNT_BUFFERFLAGS enumeration


## -description



The <b>_AUDCLNT_BUFFERFLAGS</b> enumeration defines flags that indicate the status of an audio endpoint buffer.




## -enum-fields




### -field AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY

The data in the packet is not correlated with the previous packet's device position; this is possibly due to a stream state transition or timing glitch.


### -field AUDCLNT_BUFFERFLAGS_SILENT

Treat all of the data in the packet as silence and ignore the actual data values. For more information about the use of this flag, see <a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a> and <a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>.


### -field AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR

The time at which the device's stream position was recorded is uncertain. Thus, the client might be unable to accurately set the time stamp for the current data packet.


## -remarks



The <a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a> and <a href="https://msdn.microsoft.com/19d89b5e-2e73-4693-b970-7ebf452ef9a1">IAudioRenderClient::ReleaseBuffer</a> methods use the constants defined in the <b>_AUDCLNT_BUFFERFLAGS</b> enumeration. 




## -see-also




<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/4298f584-39ce-4138-994a-0e551370429f">IAudioCaptureClient::GetBuffer</a>



<a href="https://msdn.microsoft.com/19d89b5e-2e73-4693-b970-7ebf452ef9a1">IAudioRenderClient::ReleaseBuffer</a>
 

 

