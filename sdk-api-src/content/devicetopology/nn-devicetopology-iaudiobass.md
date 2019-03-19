---
UID: NN:devicetopology.IAudioBass
title: IAudioBass (devicetopology.h)
author: windows-sdk-content
description: The IAudioBass interface provides access to a hardware bass-level control.
old-location: coreaudio\iaudiobass.htm
tech.root: CoreAudio
ms.assetid: 036ca996-8612-4905-9afa-a4c3b4624652
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioBass, IAudioBass interface [Core Audio], IAudioBass interface [Core Audio],described, coreaudio.iaudiobass, devicetopology/IAudioBass
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioBass interface


## -description



The <b>IAudioBass</b> interface provides access to a hardware bass-level control. The client obtains a reference to the <b>IAudioBass</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioBass. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioBass</b> interface. Only a subunit object that represents a hardware function for controlling the level of the bass frequencies in each channel will support this interface.




## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>



<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>
 

 

