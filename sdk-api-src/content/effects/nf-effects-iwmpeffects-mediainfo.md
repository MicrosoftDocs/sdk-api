---
UID: NF:effects.IWMPEffects.MediaInfo
title: IWMPEffects::MediaInfo
author: windows-sdk-content
description: The MediaInfo method sends channel and sample rate data to the visualization.
old-location: wmp\iwmpeffects_mediainfo.htm
tech.root: WMP
ms.assetid: 1267cb11-1b45-4f38-ad3c-02213405ed66
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EffectsMediaInfo, IWMPEffects interface [Windows Media Player],MediaInfo method, IWMPEffects.MediaInfo, IWMPEffects::MediaInfo, MediaInfo, MediaInfo method [Windows Media Player], MediaInfo method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::MediaInfo, wmp.iwmpeffects_mediainfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.MediaInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEffects::MediaInfo


## -description



The <b>MediaInfo</b> method sends channel and sample rate data to the visualization.




## -parameters




### -param lChannelCount [in]

<b>Long</b> integer containing the number of channels (one for mono, or two for stereo).


### -param lSampleRate [in]

<b>Long</b> integer containing the sample rate in hertz (Hz). For example, a value of 22500 would specify a rate of 22.5KHz.


### -param bstrTitle [in]

<b>String</b> specifying the title.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

