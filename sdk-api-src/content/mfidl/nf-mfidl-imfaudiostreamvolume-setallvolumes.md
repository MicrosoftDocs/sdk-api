---
UID: NF:mfidl.IMFAudioStreamVolume.SetAllVolumes
title: IMFAudioStreamVolume::SetAllVolumes
author: windows-sdk-content
description: Sets the individual volume levels for all of the channels in the audio stream.
old-location: mf\imfaudiostreamvolume_setallvolumes.htm
tech.root: medfound
ms.assetid: 6c278693-5a2f-4aa2-b477-3b3014b2cc89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 6c278693-5a2f-4aa2-b477-3b3014b2cc89, IMFAudioStreamVolume interface [Media Foundation],SetAllVolumes method, IMFAudioStreamVolume.SetAllVolumes, IMFAudioStreamVolume::SetAllVolumes, SetAllVolumes, SetAllVolumes method [Media Foundation], SetAllVolumes method [Media Foundation],IMFAudioStreamVolume interface, mf.imfaudiostreamvolume_setallvolumes, mfidl/IMFAudioStreamVolume::SetAllVolumes
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
 - IMFAudioStreamVolume.SetAllVolumes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioStreamVolume::SetAllVolumes


## -description



Sets the individual volume levels for all of the channels in the audio stream.




## -parameters




### -param dwCount [in]

Number of elements in the <i>pfVolumes</i> array. The value must equal the number of channels. To get the number of channels, call <a href="https://msdn.microsoft.com/d19a56db-cd5f-4a19-98f0-42327c259b01">IMFAudioStreamVolume::GetChannelCount</a>.


### -param pfVolumes [in]

Address of an array of size <i>dwCount</i>, allocated by the caller. The array specifies the volume levels for all of the channels. Before calling the method, set each element of the array to the desired volume level for the channel.


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
 

 

