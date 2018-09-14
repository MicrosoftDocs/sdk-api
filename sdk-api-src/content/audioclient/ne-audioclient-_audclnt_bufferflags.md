---
UID: NE:audioclient._AUDCLNT_BUFFERFLAGS
title: "_AUDCLNT_BUFFERFLAGS"
author: windows-sdk-content
description: The _AUDCLNT_BUFFERFLAGS enumeration defines flags that indicate the status of an audio endpoint buffer.
old-location: coreaudio\_audclnt_bufferflags.htm
tech.root: CoreAudio
ms.assetid: ac4ec901-b1e2-4c4e-b9fc-1808d5338d15
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY, AUDCLNT_BUFFERFLAGS_SILENT, AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR, _AUDCLNT_BUFFERFLAGS, _AUDCLNT_BUFFERFLAGS , _AUDCLNT_BUFFERFLAGS enumeration [Core Audio], audioclient/AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY, audioclient/AUDCLNT_BUFFERFLAGS_SILENT, audioclient/AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR, audioclient/_AUDCLNT_BUFFERFLAGS, coreaudio._audclnt_bufferflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioclient.h
api_name:
 - _AUDCLNT_BUFFERFLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

