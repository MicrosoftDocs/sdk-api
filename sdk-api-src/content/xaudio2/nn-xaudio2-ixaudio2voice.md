---
UID: NN:xaudio2.IXAudio2Voice
title: IXAudio2Voice
author: windows-sdk-content
description: IXAudio2Voice represents the base interface from which IXAudio2SourceVoice, IXAudio2SubmixVoice and IXAudio2MasteringVoice are derived. The methods listed below are common to all voice subclasses.
old-location: xaudio2\ixaudio2voice.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IXAudio2Voice, IXAudio2Voice Interface, IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs], IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2voice, xaudio2/IXAudio2Voice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2Voice Interface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice interface


## -description


<b>IXAudio2Voice</b> represents the base interface from which <a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>, <a href="https://msdn.microsoft.com/EBEF26DE-BEAB-4E1F-9C54-2EC01449F413">IXAudio2SubmixVoice</a> and <a href="https://msdn.microsoft.com/96D8A15E-5090-4D67-982D-ACE99CEC4379">IXAudio2MasteringVoice</a> are derived. The methods listed below are common to all voice subclasses.
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>IXAudio2Voice Interface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03C825B8-BC7B-4A9F-B514-2C1C3684FAD9">DestroyVoice</a>
</td>
<td align="left" width="63%">
Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5613C03D-4447-4779-8619-F3F562140B5A">DisableEffect</a>
</td>
<td align="left" width="63%">
Disables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA5B0467-D811-4A42-99B1-9F7DCFECA979">EnableEffect</a>
</td>
<td align="left" width="63%">
Enables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A0ED638C-9C20-4401-A204-9F8747044DBA">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Returns the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75CC5E5D-74B2-4972-9E1D-D6CB4A3034CD">GetEffectParameters</a>
</td>
<td align="left" width="63%">
Returns the current effect-specific parameters of a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73AEBC14-F044-4914-9ED5-2E438268373E">GetEffectState</a>
</td>
<td align="left" width="63%">
Returns the running state of the effect at a specified position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E5B3896-A415-4E06-94EB-F9205B3CFB32">GetFilterParameters</a>
</td>
<td align="left" width="63%">
Gets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/146A6338-40E9-489D-B5E9-679D328C75C7">GetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Returns the filter parameters from one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6FA23BF5-E79E-404B-A54D-514EEAA4A668">GetOutputMatrix</a>
</td>
<td align="left" width="63%">
Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33EFF71F-FA55-4D7C-A727-35C78774DBFA">GetVoiceDetails</a>
</td>
<td align="left" width="63%">
Returns information about the creation flags, input channels, and sample rate of a voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39389E49-95C9-48D2-8B35-0F2E1D52A43B">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current overall volume level of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DE09972-4FBD-41F5-BDB7-75627CBDA35A">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6CA630E6-66D5-495C-808D-79EE5E85D92B">SetEffectChain</a>
</td>
<td align="left" width="63%">
Replaces the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7A5217AE-D7D6-4D92-A14E-DA36854F4D3E">SetEffectParameters</a>
</td>
<td align="left" width="63%">
Sets parameters for a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56ACB3DB-58E0-4A57-A97F-31EFA8929A7E">SetFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A707A64A-D929-4387-AABC-30E7AAECB99B">SetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the filter parameters on one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ECE4A2B-89DF-4D76-BBE4-C930EBB5F3EA">SetOutputMatrix</a>
</td>
<td align="left" width="63%">
Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2AAF9A0D-2CDF-4A91-9620-3328494E0162">SetOutputVoices</a>
</td>
<td align="left" width="63%">
Designates a new set of submix or mastering voices to receive the output of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D744E313-4281-4184-97E9-3FAB0F652871">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the overall volume level for the voice.

</td>
</tr>
</table> 


## -members

The <b>IXAudio2Voice Interface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03C825B8-BC7B-4A9F-B514-2C1C3684FAD9">DestroyVoice</a>
</td>
<td align="left" width="63%">
Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5613C03D-4447-4779-8619-F3F562140B5A">DisableEffect</a>
</td>
<td align="left" width="63%">
Disables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA5B0467-D811-4A42-99B1-9F7DCFECA979">EnableEffect</a>
</td>
<td align="left" width="63%">
Enables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A0ED638C-9C20-4401-A204-9F8747044DBA">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Returns the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75CC5E5D-74B2-4972-9E1D-D6CB4A3034CD">GetEffectParameters</a>
</td>
<td align="left" width="63%">
Returns the current effect-specific parameters of a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73AEBC14-F044-4914-9ED5-2E438268373E">GetEffectState</a>
</td>
<td align="left" width="63%">
Returns the running state of the effect at a specified position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E5B3896-A415-4E06-94EB-F9205B3CFB32">GetFilterParameters</a>
</td>
<td align="left" width="63%">
Gets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/146A6338-40E9-489D-B5E9-679D328C75C7">GetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Returns the filter parameters from one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6FA23BF5-E79E-404B-A54D-514EEAA4A668">GetOutputMatrix</a>
</td>
<td align="left" width="63%">
Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33EFF71F-FA55-4D7C-A727-35C78774DBFA">GetVoiceDetails</a>
</td>
<td align="left" width="63%">
Returns information about the creation flags, input channels, and sample rate of a voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39389E49-95C9-48D2-8B35-0F2E1D52A43B">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current overall volume level of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DE09972-4FBD-41F5-BDB7-75627CBDA35A">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6CA630E6-66D5-495C-808D-79EE5E85D92B">SetEffectChain</a>
</td>
<td align="left" width="63%">
Replaces the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7A5217AE-D7D6-4D92-A14E-DA36854F4D3E">SetEffectParameters</a>
</td>
<td align="left" width="63%">
Sets parameters for a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56ACB3DB-58E0-4A57-A97F-31EFA8929A7E">SetFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A707A64A-D929-4387-AABC-30E7AAECB99B">SetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the filter parameters on one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ECE4A2B-89DF-4D76-BBE4-C930EBB5F3EA">SetOutputMatrix</a>
</td>
<td align="left" width="63%">
Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2AAF9A0D-2CDF-4A91-9620-3328494E0162">SetOutputVoices</a>
</td>
<td align="left" width="63%">
Designates a new set of submix or mastering voices to receive the output of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D744E313-4281-4184-97E9-3FAB0F652871">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the overall volume level for the voice.

</td>
</tr>
</table>Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.

Disables the effect at a given position in the effect chain of the voice.

Enables the effect at a given position in the effect chain of the voice.

Returns the volume levels for the voice, per channel.

Returns the current effect-specific parameters of a given effect in the voice's effect chain.

Returns the running state of the effect at a specified position in the effect chain of the voice.

Gets the voice's filter parameters.

Returns the filter parameters from one of this voice's sends.

Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

Returns information about the creation flags, input channels, and sample rate of a voice.

Gets the current overall volume level of the voice.

Sets the volume levels for the voice, per channel.

Replaces the effect chain of the voice.

Sets parameters for a given effect in the voice's effect chain.

Sets the voice's filter parameters.

Sets the filter parameters on one of this voice's sends.

Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

Designates a new set of submix or mastering voices to receive the output of the voice.

Sets the overall volume level for the voice.

 

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">XAudio2 Interfaces</a>
 

 

