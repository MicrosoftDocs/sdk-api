---
UID: NN:devicetopology.IAudioBass
title: IAudioBass (devicetopology.h)
author: windows-sdk-content
description: The IAudioBass interface provides access to a hardware bass-level control.
old-location: coreaudio\iaudiobass.htm
tech.root: CoreAudio
ms.assetid: 036ca996-8612-4905-9afa-a4c3b4624652
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioBass, IAudioBass interface [Core Audio], IAudioBass interface [Core Audio],described, coreaudio.iaudiobass, devicetopology/IAudioBass
ms.topic: interface
f1_keywords: 
 - "devicetopology/IAudioBass"
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioBass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioBass interface


## -description



The <b>IAudioBass</b> interface provides access to a hardware bass-level control. The client obtains a reference to the <b>IAudioBass</b> interface of a subunit by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioBass. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioBass</b> interface. Only a subunit object that represents a hardware function for controlling the level of the bass frequencies in each channel will support this interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>
 

 

