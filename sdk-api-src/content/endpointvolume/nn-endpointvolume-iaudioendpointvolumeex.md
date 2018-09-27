---
UID: NN:endpointvolume.IAudioEndpointVolumeEx
title: IAudioEndpointVolumeEx
author: windows-sdk-content
description: The IAudioEndpointVolumeEx interface provides volume controls on the audio stream to or from a device endpoint.
old-location: coreaudio\iaudioendpointvolumeex.htm
tech.root: CoreAudio
ms.assetid: 905ef0c9-ac32-4dfd-a25a-820cafa04815
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAudioEndpointVolumeEx, IAudioEndpointVolumeEx interface [Core Audio], IAudioEndpointVolumeEx interface [Core Audio],described, coreaudio.iaudioendpointvolumeex, endpointvolume/IAudioEndpointVolumeEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolumeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointVolumeEx interface


## -description


The <b>IAudioEndpointVolumeEx</b> interface provides volume controls on the audio stream to or from a device endpoint.

A client obtains a reference to the <b>IAudioEndpointVolumeEx</b> interface of an endpoint device by calling the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioEndpointVolumeEx.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointVolumeEx</b> interface inherits from <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a>. <b>IAudioEndpointVolumeEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointVolumeEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/869fe1cc-aa32-45e5-899f-3ae0d0f1b256">GetVolumeRangeChannel</a>
</td>
<td align="left" width="63%">
Gets the volume range for a specified channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79">EndpointVolume API</a>



<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a>



<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>



<a href="https://msdn.microsoft.com/360211f2-de82-4ff5-896c-dee1d60cb7b7">ISimpleAudioVolume Interface</a>
 

 

