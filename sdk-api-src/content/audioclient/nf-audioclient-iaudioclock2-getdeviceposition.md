---
UID: NF:audioclient.IAudioClock2.GetDevicePosition
title: IAudioClock2::GetDevicePosition (audioclient.h)
description: The GetDevicePosition method gets the current device position, in frames, directly from the hardware.
helpviewer_keywords: ["GetDevicePosition","GetDevicePosition method [Core Audio]","GetDevicePosition method [Core Audio]","IAudioClock2 interface","IAudioClock2 interface [Core Audio]","GetDevicePosition method","IAudioClock2.GetDevicePosition","IAudioClock2::GetDevicePosition","audioclient/IAudioClock2::GetDevicePosition","coreaudio.iaudioclock2_getdeviceposition"]
old-location: coreaudio\iaudioclock2_getdeviceposition.htm
tech.root: CoreAudio
ms.assetid: 2767056d-59dc-4f6e-b0f7-e37b3fed9581
ms.date: 12/05/2018
ms.keywords: GetDevicePosition, GetDevicePosition method [Core Audio], GetDevicePosition method [Core Audio],IAudioClock2 interface, IAudioClock2 interface [Core Audio],GetDevicePosition method, IAudioClock2.GetDevicePosition, IAudioClock2::GetDevicePosition, audioclient/IAudioClock2::GetDevicePosition, coreaudio.iaudioclock2_getdeviceposition
req.header: audioclient.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioClock2::GetDevicePosition
 - audioclient/IAudioClock2::GetDevicePosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClock2.GetDevicePosition
---

# IAudioClock2::GetDevicePosition


## -description

The <b>GetDevicePosition</b> method gets the current device position, in frames, directly from the hardware.

## -parameters

### -param DevicePosition [out]

Receives the device position, in frames. The received position is an unprocessed value that the method obtains directly from the hardware. For more information, see Remarks.

### -param QPCPosition [out]

Receives the value of the performance counter at the time that the audio endpoint device read the device position retrieved in the <i>DevicePosition</i> parameter in response to the <b>GetDevicePosition</b> call.  
					 <b>GetDevicePosition</b> converts the counter value to 100-nanosecond time units before writing it to <i>QPCPosition</i>.
					<i>QPCPosition</i> can be <b>NULL</b> if the client does not require the performance counter value.
				For more information, see Remarks.

## -returns

If the method succeeds, it returns S_OK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>DevicePosition</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint has been disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_S_POSITION_STALLED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a> method has not been called for this stream.

</td>
</tr>
</table>

## -remarks

This method only applies to shared-mode streams. 

This method retrieves two correlated stream-position values:
        
      
        

<ul>
<li>Device position. The client retrieves the unprocessed device position in <i>DevicePosition</i>. This is the stream position of the sample that is currently playing through the speakers (for a rendering stream) or being recorded through the microphone (for a capture stream). The sampling rate of the device endpoint may be different from the sampling rate of the mix format used by the client.
					To retrieve the device position from the client, call <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getposition">IAudioClock::GetPosition</a>.
				</li>
<li>Performance counter. The client retrieves the performance counter in <i>QPCPosition</i>. <b>GetDevicePosition</b> obtains the counter value by calling the <b>QueryPerformanceCounter</b> function at the time that the audio endpoint device stores the stream position in the <i>DevicePosition</i> parameter of the <b>GetDevicePosition</b> method. <b>GetDevicePosition</b> converts the counter value to 100-nanosecond time units. For more information about <b>QueryPerformanceCounter</b> and <b>QueryPerformanceFrequency</b>, see the Windows SDK documentation.</li>
</ul>
Given the device position and the performance counter at the time of the <b>GetDevicePosition</b> call, the client can get a more timely estimate of the device position at a later time by calling <b>QueryPerformanceCounter</b> to obtain the current performance counter, and extrapolating the device position based on how far the counter has advanced since the original device position was recorded. The client can call the <b>QueryPerformanceCounter</b> function to get the frequency of the clock that increments the counter. Before comparing the raw counter value obtained from <b>QueryPerformanceCounter</b> to the value retrieved by <b>GetDevicePosition</b>, convert the raw counter value to 100-nanosecond time units as follows:

<ol>
<li>Multiply the raw counter value by 10,000,000.</li>
<li>Divide the result by the counter frequency obtained from <b>QueryPerformanceFrequency</b>.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2">IAudioClock2</a>