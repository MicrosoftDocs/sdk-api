---
UID: NF:mfidl.IMFAudioStreamVolume.GetChannelCount
title: IMFAudioStreamVolume::GetChannelCount
author: windows-sdk-content
description: Retrieves the number of channels in the audio stream.
old-location: mf\imfaudiostreamvolume_getchannelcount.htm
tech.root: medfound
ms.assetid: d19a56db-cd5f-4a19-98f0-42327c259b01
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetChannelCount, GetChannelCount method [Media Foundation], GetChannelCount method [Media Foundation],IMFAudioStreamVolume interface, IMFAudioStreamVolume interface [Media Foundation],GetChannelCount method, IMFAudioStreamVolume.GetChannelCount, IMFAudioStreamVolume::GetChannelCount, d19a56db-cd5f-4a19-98f0-42327c259b01, mf.imfaudiostreamvolume_getchannelcount, mfidl/IMFAudioStreamVolume::GetChannelCount
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
 - IMFAudioStreamVolume.GetChannelCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioStreamVolume::GetChannelCount


## -description



Retrieves the number of channels in the audio stream.




## -parameters




### -param pdwCount [out]

Receives the number of channels in the audio stream.


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
 

 

