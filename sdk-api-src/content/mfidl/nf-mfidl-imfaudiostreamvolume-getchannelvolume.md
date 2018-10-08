---
UID: NF:mfidl.IMFAudioStreamVolume.GetChannelVolume
title: IMFAudioStreamVolume::GetChannelVolume
author: windows-sdk-content
description: Retrieves the volume level for a specified channel in the audio stream.
old-location: mf\imfaudiostreamvolume_getchannelvolume.htm
tech.root: medfound
ms.assetid: 5cfcc3a8-2911-45a3-8322-bf4e3b023dd2
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 5cfcc3a8-2911-45a3-8322-bf4e3b023dd2, GetChannelVolume, GetChannelVolume method [Media Foundation], GetChannelVolume method [Media Foundation],IMFAudioStreamVolume interface, IMFAudioStreamVolume interface [Media Foundation],GetChannelVolume method, IMFAudioStreamVolume.GetChannelVolume, IMFAudioStreamVolume::GetChannelVolume, mf.imfaudiostreamvolume_getchannelvolume, mfidl/IMFAudioStreamVolume::GetChannelVolume
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioStreamVolume.GetChannelVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioStreamVolume::GetChannelVolume


## -description



Retrieves the volume level for a specified channel in the audio stream.




## -parameters




### -param dwIndex [in]

Zero-based index of the audio channel. To get the number of channels, call <a href="https://msdn.microsoft.com/d19a56db-cd5f-4a19-98f0-42327c259b01">IMFAudioStreamVolume::GetChannelCount</a>.


### -param pfLevel [out]

Receives the volume level for the channel.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f06ed262-a2ec-4688-b477-877d04cf1892">IMFAudioStreamVolume</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

