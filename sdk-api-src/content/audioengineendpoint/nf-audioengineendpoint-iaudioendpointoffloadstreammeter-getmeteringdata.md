---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamMeter.GetMeteringData
title: IAudioEndpointOffloadStreamMeter::GetMeteringData
author: windows-sdk-content
description: The GetMeteringData method retrieves general information about the available audio channels in the offloaded stream.
old-location: coreaudio\iaudioendpointoffloadstreammeter_getmeteringdata.htm
old-project: CoreAudio
ms.assetid: 31F76D5B-D047-4D0E-AA22-DCC1E2E36561
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetMeteringData, GetMeteringData method [Core Audio], GetMeteringData method [Core Audio],IAudioEndpointOffloadStreamMeter interface, IAudioEndpointOffloadStreamMeter interface [Core Audio],GetMeteringData method, IAudioEndpointOffloadStreamMeter.GetMeteringData, IAudioEndpointOffloadStreamMeter::GetMeteringData, audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeteringData, coreaudio.iaudioendpointoffloadstreammeter_getmeteringdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamMeter.GetMeteringData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpointOffloadStreamMeter::GetMeteringData


## -description


The <b>GetMeteringData</b> method retrieves general information about the available audio channels in the offloaded stream.


## -parameters




### -param u32ChannelCount [in]

Indicates the number of available audio channels in the offloaded audio stream.


### -param pf32PeakValues [out]

A pointer to the peak values for the audio channels in the offloaded audio stream.


## -returns



The <b>GetMeteringData</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.





## -see-also




<a href="https://msdn.microsoft.com/B19413F9-1DE9-4940-B0A1-11E5278F084B">IAudioEndpointOffloadStreamMeter</a>
 

 

