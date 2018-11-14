---
UID: NN:xaudio2.IXAudio2MasteringVoice
title: IXAudio2MasteringVoice
author: windows-sdk-content
description: A mastering voice is used to represent the audio output device.
old-location: xaudio2\ixaudio2masteringvoice.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2masteringvoice.IXAudio2MasteringVoice
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IXAudio2MasteringVoice, IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs], IXAudio2MasteringVoice interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2masteringvoice, xaudio2/IXAudio2MasteringVoice
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
 - IXAudio2MasteringVoice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2MasteringVoice interface


## -description


A mastering voice is used to represent the audio output device.

Data buffers cannot be submitted directly to mastering voices, but data submitted to other types of voices must be directed to a mastering voice to be heard. 


<b>IXAudio2MasteringVoice</b> inherits directly from <a href="https://msdn.microsoft.com/en-us/library/Ee415917(v=VS.85).aspx">IXAudio2Voice</a>, but does not implement methods specific to mastering voices. The interface type exists solely because some of the base class methods are implemented differently for mastering voices. Having a separate type for these voices helps client code to distinguish the different voice types and to benefit from C++ type safety.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAudio2MasteringVoice</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Ee415917(v=VS.85).aspx">IXAudio2Voice</a>. <b>IXAudio2MasteringVoice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAudio2MasteringVoice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh405046(v=VS.85).aspx">GetChannelMask</a>
</td>
<td align="left" width="63%">
Returns the channel mask for the mastering voice.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415917(v=VS.85).aspx">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">XAudio2 Interfaces</a>
 

 

