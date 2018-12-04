---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.SetEndOfStream
title: ISpatialAudioObjectBase::SetEndOfStream
author: windows-sdk-content
description: Instructs the system that the final block of audio data has been submitted for the ISpatialAudioObject so that the object can be deactivated and it's resources reused.
old-location: coreaudio\ispatialaudioobject_setendofstream.htm
tech.root: CoreAudio
ms.assetid: 17294E5D-04D7-43B9-AD41-392344309308
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISpatialAudioObjectBase interface [Core Audio],SetEndOfStream method, ISpatialAudioObjectBase.SetEndOfStream, ISpatialAudioObjectBase::SetEndOfStream, SetEndOfStream, SetEndOfStream method [Core Audio], SetEndOfStream method [Core Audio],ISpatialAudioObjectBase interface, coreaudio.ispatialaudioobject_setendofstream, spatialaudioclient/ISpatialAudioObjectBase::SetEndOfStream
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
 - ISpatialAudioObjectBase.SetEndOfStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectBase::SetEndOfStream


## -description


Instructs the system that the final block of audio data has been  submitted for the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> so that the object can be deactivated and it's resources reused. 


## -parameters




### -param frameCount [in]

The number of audio frames in the audio buffer that should be included in the final processing pass. This number may be smaller than or equal to the value returned in  the <i>frameCountPerBuffer</i> parameter to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a>. 


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

<a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> was not called before the call to <b>SetEndOfStream</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">SetEndOfStream</a> was called either explicitly or implicitly in a previous audio processing pass. <b>SetEndOfStream</b> is called implicitly by the system if <b>GetBuffer</b> is not called within an audio processing pass (between calls to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> and <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>).

</td>
</tr>
</table>
 




## -remarks



Call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> after calling <b>SetEndOfStream</b> to make free the audio object resources for future use.




## -see-also




<a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>



<a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>
 

 

