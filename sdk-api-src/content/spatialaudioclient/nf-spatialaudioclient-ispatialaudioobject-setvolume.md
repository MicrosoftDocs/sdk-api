---
UID: NF:spatialaudioclient.ISpatialAudioObject.SetVolume
title: ISpatialAudioObject::SetVolume
author: windows-sdk-content
description: Sets an audio amplitude multiplier that will be applied to the audio data provided by the ISpatialAudioObject before it is submitted to the audio rendering engine.
old-location: coreaudio\ispatialaudioobject_setvolume.htm
tech.root: CoreAudio
ms.assetid: DC1B4B9C-BFE0-4308-AD34-500A30C5744F
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ISpatialAudioObject interface [Core Audio],SetVolume method, ISpatialAudioObject.SetVolume, ISpatialAudioObject::SetVolume, SetVolume, SetVolume method [Core Audio], SetVolume method [Core Audio],ISpatialAudioObject interface, coreaudio.ispatialaudioobject_setvolume, spatialaudioclient/ISpatialAudioObject::SetVolume
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObject.SetVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObject::SetVolume


## -description


Sets an audio amplitude multiplier that will be applied to the audio data provided by the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> before it is submitted to the audio rendering engine.


## -parameters




### -param volume [in]

The amplitude multiplier for audio data. This must be a value between 0.0 and 1.0.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetVolume</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStreamBase::BeginUpdatingAudioObjects</a> and <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">ISpatialAudioObjectRenderStreamBase::EndUpdatingAudioObjects</a>).

</td>
</tr>
</table>
 




## -remarks



If <b>SetVolume</b> is never called, the default value of 1.0 is used. After <b>SetVolume</b> is called, the volume that is set will be used for the audio object until the volume is changed with another call to <b>SetVolume</b>.




## -see-also




<a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>
 

 

