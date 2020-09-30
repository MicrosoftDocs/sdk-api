---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamMeter.GetMeterChannelCount
title: IAudioEndpointOffloadStreamMeter::GetMeterChannelCount (audioengineendpoint.h)
description: Gets the number of available audio channels in the offloaded stream that can be metered.
helpviewer_keywords: ["GetMeterChannelCount","GetMeterChannelCount method [Core Audio]","GetMeterChannelCount method [Core Audio]","IAudioEndpointOffloadStreamMeter interface","IAudioEndpointOffloadStreamMeter interface [Core Audio]","GetMeterChannelCount method","IAudioEndpointOffloadStreamMeter.GetMeterChannelCount","IAudioEndpointOffloadStreamMeter::GetMeterChannelCount","audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeterChannelCount","coreaudio.iaudioendpointoffloadstreammeter_getmeterchannelcount"]
old-location: coreaudio\iaudioendpointoffloadstreammeter_getmeterchannelcount.htm
tech.root: CoreAudio
ms.assetid: 52C34D08-8ACD-4E3A-80F4-4FA823E11D9C
ms.date: 12/05/2018
ms.keywords: GetMeterChannelCount, GetMeterChannelCount method [Core Audio], GetMeterChannelCount method [Core Audio],IAudioEndpointOffloadStreamMeter interface, IAudioEndpointOffloadStreamMeter interface [Core Audio],GetMeterChannelCount method, IAudioEndpointOffloadStreamMeter.GetMeterChannelCount, IAudioEndpointOffloadStreamMeter::GetMeterChannelCount, audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeterChannelCount, coreaudio.iaudioendpointoffloadstreammeter_getmeterchannelcount
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointOffloadStreamMeter::GetMeterChannelCount
 - audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeterChannelCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamMeter.GetMeterChannelCount
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

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointoffloadstreammeter">IAudioEndpointOffloadStreamMeter</a>