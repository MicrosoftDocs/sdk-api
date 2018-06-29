---
UID: NN:xaudio2.IXAudio2Voice
title: IXAudio2Voice
author: windows-sdk-content
description: IXAudio2Voice represents the base interface from which IXAudio2SourceVoice, IXAudio2SubmixVoice and IXAudio2MasteringVoice are derived. The methods listed below are common to all voice subclasses.
old-location: xaudio2\ixaudio2voice.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: IXAudio2Voice, IXAudio2Voice Interface, IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs], IXAudio2Voice Interface interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2voice, xaudio2/IXAudio2Voice
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XAUDIO2_FILTER_TYPE
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2Voice interface


## -description


<b>IXAudio2Voice</b> represents the base interface from which <a href="https://msdn.microsoft.com/library/Ee415914(v=VS.85).aspx">IXAudio2SourceVoice</a>, <a href="https://msdn.microsoft.com/library/Ee415915(v=VS.85).aspx">IXAudio2SubmixVoice</a> and <a href="https://msdn.microsoft.com/library/Ee415912(v=VS.85).aspx">IXAudio2MasteringVoice</a> are derived. The methods listed below are common to all voice subclasses.
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
<a href="https://msdn.microsoft.com/library/Ee418481(v=VS.85).aspx">DestroyVoice</a>
</td>
<td align="left" width="63%">
Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418583(v=VS.85).aspx">DisableEffect</a>
</td>
<td align="left" width="63%">
Disables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418584(v=VS.85).aspx">EnableEffect</a>
</td>
<td align="left" width="63%">
Enables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418585(v=VS.85).aspx">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Returns the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418586(v=VS.85).aspx">GetEffectParameters</a>
</td>
<td align="left" width="63%">
Returns the current effect-specific parameters of a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418587(v=VS.85).aspx">GetEffectState</a>
</td>
<td align="left" width="63%">
Returns the running state of the effect at a specified position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418588(v=VS.85).aspx">GetFilterParameters</a>
</td>
<td align="left" width="63%">
Gets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418589(v=VS.85).aspx">GetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Returns the filter parameters from one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418590(v=VS.85).aspx">GetOutputMatrix</a>
</td>
<td align="left" width="63%">
Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418591(v=VS.85).aspx">GetVoiceDetails</a>
</td>
<td align="left" width="63%">
Returns information about the creation flags, input channels, and sample rate of a voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418592(v=VS.85).aspx">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current overall volume level of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418593(v=VS.85).aspx">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418594(v=VS.85).aspx">SetEffectChain</a>
</td>
<td align="left" width="63%">
Replaces the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418595(v=VS.85).aspx">SetEffectParameters</a>
</td>
<td align="left" width="63%">
Sets parameters for a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418596(v=VS.85).aspx">SetFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418597(v=VS.85).aspx">SetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the filter parameters on one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418598(v=VS.85).aspx">SetOutputMatrix</a>
</td>
<td align="left" width="63%">
Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418599(v=VS.85).aspx">SetOutputVoices</a>
</td>
<td align="left" width="63%">
Designates a new set of submix or mastering voices to receive the output of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418600(v=VS.85).aspx">SetVolume</a>
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
<a href="https://msdn.microsoft.com/library/Ee418481(v=VS.85).aspx">DestroyVoice</a>
</td>
<td align="left" width="63%">
Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418583(v=VS.85).aspx">DisableEffect</a>
</td>
<td align="left" width="63%">
Disables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418584(v=VS.85).aspx">EnableEffect</a>
</td>
<td align="left" width="63%">
Enables the effect at a given position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418585(v=VS.85).aspx">GetChannelVolumes</a>
</td>
<td align="left" width="63%">
Returns the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418586(v=VS.85).aspx">GetEffectParameters</a>
</td>
<td align="left" width="63%">
Returns the current effect-specific parameters of a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418587(v=VS.85).aspx">GetEffectState</a>
</td>
<td align="left" width="63%">
Returns the running state of the effect at a specified position in the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418588(v=VS.85).aspx">GetFilterParameters</a>
</td>
<td align="left" width="63%">
Gets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418589(v=VS.85).aspx">GetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Returns the filter parameters from one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418590(v=VS.85).aspx">GetOutputMatrix</a>
</td>
<td align="left" width="63%">
Gets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418591(v=VS.85).aspx">GetVoiceDetails</a>
</td>
<td align="left" width="63%">
Returns information about the creation flags, input channels, and sample rate of a voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418592(v=VS.85).aspx">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current overall volume level of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418593(v=VS.85).aspx">SetChannelVolumes</a>
</td>
<td align="left" width="63%">
Sets the volume levels for the voice, per channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418594(v=VS.85).aspx">SetEffectChain</a>
</td>
<td align="left" width="63%">
Replaces the effect chain of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418595(v=VS.85).aspx">SetEffectParameters</a>
</td>
<td align="left" width="63%">
Sets parameters for a given effect in the voice's effect chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418596(v=VS.85).aspx">SetFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the voice's filter parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418597(v=VS.85).aspx">SetOutputFilterParameters</a>
</td>
<td align="left" width="63%">
Sets the filter parameters on one of this voice's sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418598(v=VS.85).aspx">SetOutputMatrix</a>
</td>
<td align="left" width="63%">
Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418599(v=VS.85).aspx">SetOutputVoices</a>
</td>
<td align="left" width="63%">
Designates a new set of submix or mastering voices to receive the output of the voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Ee418600(v=VS.85).aspx">SetVolume</a>
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
 

 

