---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamMeter.GetMeterChannelCount
title: IAudioEndpointOffloadStreamMeter::GetMeterChannelCount
author: windows-sdk-content
description: Gets the number of available audio channels in the offloaded stream that can be metered.
old-location: coreaudio\iaudioendpointoffloadstreammeter_getmeterchannelcount.htm
old-project: CoreAudio
ms.assetid: 52C34D08-8ACD-4E3A-80F4-4FA823E11D9C
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetMeterChannelCount, GetMeterChannelCount method [Core Audio], GetMeterChannelCount method [Core Audio],IAudioEndpointOffloadStreamMeter interface, IAudioEndpointOffloadStreamMeter interface [Core Audio],GetMeterChannelCount method, IAudioEndpointOffloadStreamMeter.GetMeterChannelCount, IAudioEndpointOffloadStreamMeter::GetMeterChannelCount, audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeterChannelCount, coreaudio.iaudioendpointoffloadstreammeter_getmeterchannelcount
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
req.typenames: AE_POSITION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioengineendpoint.h
api_name:
-	IAudioEndpointOffloadStreamMeter.GetMeterChannelCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpointOffloadStreamMeter::GetMeterChannelCount


## -description


Gets the number of available audio channels in the offloaded stream that can be metered.


## -parameters




### -param pu32ChannelCount [out]

A Pointer to a variable that indicates the number of available audio channels in the offloaded stream that can be metered.


## -returns



The <b>GetMeterChannelCount</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/B19413F9-1DE9-4940-B0A1-11E5278F084B">IAudioEndpointOffloadStreamMeter</a>
 

 

