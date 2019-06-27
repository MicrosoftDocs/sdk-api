---
UID: NN:audioengineendpoint.IHardwareAudioEngineBase
title: IHardwareAudioEngineBase (audioengineendpoint.h)
author: windows-sdk-content
description: The IHardwareAudioEngineBase interface is implemented by audio endpoints for the audio stack to use to configure and retrieve information about the hardware audio engine.
old-location: coreaudio\ihardwareaudioenginebase.htm
tech.root: CoreAudio
ms.assetid: 6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IHardwareAudioEngineBase, IHardwareAudioEngineBase interface [Core Audio], IHardwareAudioEngineBase interface [Core Audio],described, audioengineendpoint/IHardwareAudioEngineBase, coreaudio.ihardwareaudioenginebase
ms.topic: interface
f1_keywords: 
 - "audioengineendpoint/IHardwareAudioEngineBase"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IHardwareAudioEngineBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHardwareAudioEngineBase interface


## -description


The <b>IHardwareAudioEngineBase</b> interface is implemented by audio endpoints for the audio stack to use to configure and retrieve information about the hardware audio engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHardwareAudioEngineBase</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHardwareAudioEngineBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHardwareAudioEngineBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-ihardwareaudioenginebase-getavailableoffloadconnectorcount">GetAvailableOffloadConnectorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of available endpoints for handling offloaded audio streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-ihardwareaudioenginebase-getengineformat">GetEngineFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current data format for the hardware audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-ihardwareaudioenginebase-getgfxstate">GetGfxState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the global effects  that are currently applied to the offloaded audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-ihardwareaudioenginebase-setenginedeviceformat">SetEngineDeviceFormat</a>
</td>
<td align="left" width="63%">
Sets the data format for the hardware audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-ihardwareaudioenginebase-setgfxstate">SetGfxState</a>
</td>
<td align="left" width="63%">
Sets the state of the global effects (GFX) that are applied to the offloaded audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
 

 

