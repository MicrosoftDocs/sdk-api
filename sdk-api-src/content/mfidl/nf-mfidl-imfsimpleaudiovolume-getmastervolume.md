---
UID: NF:mfidl.IMFSimpleAudioVolume.GetMasterVolume
title: IMFSimpleAudioVolume::GetMasterVolume method
author: windows-driver-content
description: Retrieves the master volume level.
old-location: mf\imfsimpleaudiovolume_getmastervolume.htm
old-project: medfound
ms.assetid: 03ce097e-c4e5-4dac-84c0-b569efc420bc
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 03ce097e-c4e5-4dac-84c0-b569efc420bc, GetMasterVolume method [Media Foundation], GetMasterVolume method [Media Foundation], IMFSimpleAudioVolume interface, GetMasterVolume,IMFSimpleAudioVolume.GetMasterVolume, IMFSimpleAudioVolume, IMFSimpleAudioVolume interface [Media Foundation], GetMasterVolume method, IMFSimpleAudioVolume::GetMasterVolume, mf.imfsimpleaudiovolume_getmastervolume, mfidl/IMFSimpleAudioVolume::GetMasterVolume
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSimpleAudioVolume.GetMasterVolume
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSimpleAudioVolume::GetMasterVolume method


## -description



Retrieves the master volume level.




## -parameters




### -param pfLevel [out]

Receives the volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).


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



If an external event changes the master volume, the audio renderer sends an <a href="https://msdn.microsoft.com/63c37bd2-0289-407a-92f1-169eb5d2e02e">MEAudioSessionVolumeChanged</a> event, which the Media Session forwards to the application.




## -see-also




<a href="https://msdn.microsoft.com/002d85a7-8bc3-422e-8ced-1907ac121d7b">IMFSimpleAudioVolume</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

