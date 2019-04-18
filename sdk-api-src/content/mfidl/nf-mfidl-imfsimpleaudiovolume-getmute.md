---
UID: NF:mfidl.IMFSimpleAudioVolume.GetMute
title: IMFSimpleAudioVolume::GetMute (mfidl.h)
author: windows-sdk-content
description: Queries whether the audio is muted.
old-location: mf\imfsimpleaudiovolume_getmute.htm
tech.root: medfound
ms.assetid: 13907d3c-62c0-4cb8-8921-5a38a63d7d6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 13907d3c-62c0-4cb8-8921-5a38a63d7d6e, GetMute, GetMute method [Media Foundation], GetMute method [Media Foundation],IMFSimpleAudioVolume interface, IMFSimpleAudioVolume interface [Media Foundation],GetMute method, IMFSimpleAudioVolume.GetMute, IMFSimpleAudioVolume::GetMute, mf.imfsimpleaudiovolume_getmute, mfidl/IMFSimpleAudioVolume::GetMute
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
 - IMFSimpleAudioVolume.GetMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSimpleAudioVolume::GetMute


## -description



Queries whether the audio is muted.




## -parameters




### -param pbMute [out]

Receives a Boolean value. If <b>TRUE</b>, the audio is muted; otherwise, the audio is not muted.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio renderer is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
The audio renderer was removed from the pipeline.

</td>
</tr>
</table>
 




## -remarks



Calling <a href="https://msdn.microsoft.com/42b51817-3c2a-463a-a533-19c327c57354">IMFSimpleAudioVolume::SetMasterVolume</a> to set the volume does not change whether the audio is muted.




## -see-also




<a href="https://msdn.microsoft.com/002d85a7-8bc3-422e-8ced-1907ac121d7b">IMFSimpleAudioVolume</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

