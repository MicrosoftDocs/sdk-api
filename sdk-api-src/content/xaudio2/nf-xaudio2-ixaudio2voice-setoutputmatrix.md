---
UID: NF:xaudio2.IXAudio2Voice.SetOutputMatrix
title: IXAudio2Voice::SetOutputMatrix
author: windows-sdk-content
description: Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.
old-location: xaudio2\ixaudio2voice_interface_setoutputmatrix.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetOutputMatrix(IXAudio2Voice,UINT32,UINT32,const float,UINT32)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetOutputMatrix method, IXAudio2Voice.SetOutputMatrix, IXAudio2Voice::SetOutputMatrix, SetOutputMatrix, SetOutputMatrix method [XAudio2 Audio Mixing APIs], SetOutputMatrix method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_setoutputmatrix, xaudio2/IXAudio2Voice::SetOutputMatrix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2Voice.SetOutputMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xaudio2.h
: 
- IXAudio2Voice.SetOutputMatrix
: 
---

# IXAudio2Voice::SetOutputMatrix


## -description


Sets the volume level of each channel of the final output for the voice. These channels are mapped to the input channels of a specified destination voice.


## -parameters




### -param pDestinationVoice [in]

Pointer to a destination <a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a> for which to set volume levels.

<div class="alert"><b>Note</b>  If the voice sends to a single target voice then specifying NULL will cause <b>SetOutputMatrix</b> to operate on that target voice.</div>
<div> </div>

### -param SourceChannels [in]

Confirms the output channel count of the voice. This is the number of channels that are produced by the last effect in the chain.


### -param DestinationChannels [in]

Confirms the input channel count of the destination voice.


### -param pLevelMatrix [in]

Array of [<i>SourceChannels</i> × <i>DestinationChannels</i>] volume levels sent to the destination voice. The level sent from source channel <i>S</i> to destination channel <i>D</i> is specified in the form <i>pLevelMatrix</i>[<i>SourceChannels</i> × <i>D</i> + <i>S</i>]. 


For example, when rendering two-channel stereo input into 5.1 output that is weighted toward the front channels—but is absent from the center and low-frequency channels—the matrix might have the values shown in the following table.



<table>
<tr>
<th>Output</th>
<th>Left Input [Array Index]</th>
<th>Right Input [Array Index]</th>
</tr>
<tr>
<td>Left</td>
<td>1.0 [0]</td>
<td>0.0 [1]</td>
</tr>
<tr>
<td>Right</td>
<td>0.0 [2]</td>
<td>1.0 [3]</td>
</tr>
<tr>
<td>Front Center</td>
<td>0.0 [4]</td>
<td>0.0 [5]</td>
</tr>
<tr>
<td>LFE</td>
<td>0.0 [6]</td>
<td>0.0 [7]</td>
</tr>
<tr>
<td>Rear Left</td>
<td>0.8 [8]</td>
<td>0.0 [9]</td>
</tr>
<tr>
<td>Rear Right</td>
<td>0.0 [10]</td>
<td>0.8 [11]</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The left and right input are fully mapped to the output left and right channels; 80 percent of the left and right input is mapped to the rear left and right channels.</div>
<div> </div>
See Remarks for more information on volume levels.


### -param X2DEFAULT

TBD




#### - OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="https://msdn.microsoft.com/5bfd747d-af65-f619-e549-be8130748261">XAudio2 Operation Sets</a> overview for more information.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of error codes.




## -remarks



This method is valid only for source and submix voices, because mastering voices write directly to the device with no matrix mixing.



Volume levels are expressed as floating-point amplitude multipliers between -XAUDIO2_MAX_VOLUME_LEVEL and XAUDIO2_MAX_VOLUME_LEVEL (-2²⁴ to 2²⁴), with a maximum gain of 144.5 dB. A volume level of 1.0 means there is no attenuation or gain and 0 means silence. Negative levels can be used to invert the audio's phase. See <a href="https://msdn.microsoft.com/dedc2d01-af83-d7d2-5b64-743dcebc83f7">XAudio2 Volume and Pitch Control</a> for additional information on volume control.




The <a href="https://msdn.microsoft.com/1638e848-4186-5dea-18e8-5369eee544ae">X3DAudio</a> function <a href="https://msdn.microsoft.com/d6b05917-9253-4c05-a318-ff13d9a329eb">X3DAudioCalculate</a> can produce an output matrix for use with <b>SetOutputMatrix</b> based on a sound's position and a listener's position.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/6FA23BF5-E79E-404B-A54D-514EEAA4A668">IXAudio2Voice::GetOutputMatrix</a> always returns the levels most recently set by <b>IXAudio2Voice::SetOutputMatrix</b>. However, they may not actually be in effect yet: they only take effect the next time the audio engine runs after the <b>IXAudio2Voice::SetOutputMatrix</b> call (or after the corresponding <a href="https://msdn.microsoft.com/2E798B7B-AD3E-4DCD-BB88-BAD3EC64EFE1">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetOutputMatrix</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/40004128-4abb-4bcd-fe76-91276be8abec">How to: Change Voice Volume</a>



<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>
 

 

