---
UID: NN:audioengineendpoint.IHardwareAudioEngineBase
title: IHardwareAudioEngineBase
author: windows-sdk-content
description: The IHardwareAudioEngineBase interface is implemented by audio endpoints for the audio stack to use to configure and retrieve information about the hardware audio engine.
old-location: coreaudio\ihardwareaudioenginebase.htm
old-project: CoreAudio
ms.assetid: 6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IHardwareAudioEngineBase, IHardwareAudioEngineBase interface [Core Audio], IHardwareAudioEngineBase interface [Core Audio],described, audioengineendpoint/IHardwareAudioEngineBase, coreaudio.ihardwareaudioenginebase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	IHardwareAudioEngineBase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IHardwareAudioEngineBase interface


## -description


The <b>IHardwareAudioEngineBase</b> interface is implemented by audio endpoints for the audio stack to use to configure and retrieve information about the hardware audio engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHardwareAudioEngineBase</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHardwareAudioEngineBase</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/FCAFF20A-812A-4232-A86C-79D07D5AE26F">GetAvailableOffloadConnectorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of available endpoints for handling offloaded audio streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/150F8E7C-35A0-42DA-8E3D-69835153382F">GetEngineFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current data format for the hardware audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265083">GetGfxState</a>
</td>
<td align="left" width="63%">
Retrieves the state of the global effects  that are currently applied to the offloaded audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BE4644E7-DBC7-4B30-AD26-483889425195">SetEngineDeviceFormat</a>
</td>
<td align="left" width="63%">
Sets the data format for the hardware audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265089">SetGfxState</a>
</td>
<td align="left" width="63%">
Sets the state of the global effects (GFX) that are applied to the offloaded audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

