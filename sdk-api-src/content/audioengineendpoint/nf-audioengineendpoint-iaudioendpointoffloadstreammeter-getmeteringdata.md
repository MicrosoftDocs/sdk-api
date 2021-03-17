---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamMeter.GetMeteringData
title: IAudioEndpointOffloadStreamMeter::GetMeteringData (audioengineendpoint.h)
description: The GetMeteringData method retrieves general information about the available audio channels in the offloaded stream.
helpviewer_keywords: ["GetMeteringData","GetMeteringData method [Core Audio]","GetMeteringData method [Core Audio]","IAudioEndpointOffloadStreamMeter interface","IAudioEndpointOffloadStreamMeter interface [Core Audio]","GetMeteringData method","IAudioEndpointOffloadStreamMeter.GetMeteringData","IAudioEndpointOffloadStreamMeter::GetMeteringData","audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeteringData","coreaudio.iaudioendpointoffloadstreammeter_getmeteringdata"]
old-location: coreaudio\iaudioendpointoffloadstreammeter_getmeteringdata.htm
tech.root: CoreAudio
ms.assetid: 31F76D5B-D047-4D0E-AA22-DCC1E2E36561
ms.date: 12/05/2018
ms.keywords: GetMeteringData, GetMeteringData method [Core Audio], GetMeteringData method [Core Audio],IAudioEndpointOffloadStreamMeter interface, IAudioEndpointOffloadStreamMeter interface [Core Audio],GetMeteringData method, IAudioEndpointOffloadStreamMeter.GetMeteringData, IAudioEndpointOffloadStreamMeter::GetMeteringData, audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeteringData, coreaudio.iaudioendpointoffloadstreammeter_getmeteringdata
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
 - IAudioEndpointOffloadStreamMeter::GetMeteringData
 - audioengineendpoint/IAudioEndpointOffloadStreamMeter::GetMeteringData
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
 - IAudioEndpointOffloadStreamMeter.GetMeteringData
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

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointoffloadstreammeter">IAudioEndpointOffloadStreamMeter</a>