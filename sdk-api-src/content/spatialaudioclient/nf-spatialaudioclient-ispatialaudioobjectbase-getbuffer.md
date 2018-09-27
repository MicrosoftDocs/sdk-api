---
UID: NF:spatialaudioclient.ISpatialAudioObjectBase.GetBuffer
title: ISpatialAudioObjectBase::GetBuffer
author: windows-sdk-content
description: Gets a buffer that is used to supply the audio data for the ISpatialAudioObject.
old-location: coreaudio\ispatialaudioobject_getbuffer.htm
tech.root: CoreAudio
ms.assetid: CD777E2D-4CA0-4C2D-A475-22BF770DD59D
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetBuffer, GetBuffer method [Core Audio], GetBuffer method [Core Audio],ISpatialAudioObjectBase interface, ISpatialAudioObjectBase interface [Core Audio],GetBuffer method, ISpatialAudioObjectBase.GetBuffer, ISpatialAudioObjectBase::GetBuffer, coreaudio.ispatialaudioobject_getbuffer, spatialaudioclient/ISpatialAudioObjectBase::GetBuffer
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
 - ISpatialAudioObjectBase.GetBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectBase::GetBuffer


## -description


Gets a buffer that is used to supply the audio data for the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>.


## -parameters




### -param buffer [out]

The buffer into which audio data is written.


### -param bufferLength [out]

The length of the buffer in bytes. This length will be the value returned in the   <i>frameCountPerBuffer</i> parameter to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> multiplied by the value of the <b>nBlockAlign</b> field of the <a href="https://msdn.microsoft.com/f2f050d6-afe2-4647-932b-1287f4538702">WAVEFORMATEX</a> structure passed in the     <a href="https://msdn.microsoft.com/DD27FDE1-3B4B-4C11-A980-15AF60A3A75B">SpatialAudioObjectRenderStreamActivationParams</a>  
    parameter to  <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a>. 


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

<a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> was not called before the call to <b>GetBuffer</b>. This method must be called before the first time <b>GetBuffer</b> is called and after every subsequent call to <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>.

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



The first time <b>GetBuffer</b> is called after the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> is activated with a call <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a>,  
    lifetime of the spatial audio object starts.  
    To keep the spatial audio object alive after that, this <b>GetBuffer</b> must be called on every processing pass (between calls to <a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects</a> and <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a>). If <b>GetBuffer</b> is not called within an audio processing pass, <a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">SetEndOfStream</a> is called implicitly on the audio object to deactivate, and the audio object can only be reused after calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the object and then reactivating the object by calling <b>ActivateSpatialAudioObject</b> again.

The pointers retrieved by <b>GetBuffer</b> should not be used after   
    <a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects</a> has been called.




## -see-also




<a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a>



<a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>
 

 

