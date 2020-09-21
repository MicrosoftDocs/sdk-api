---
UID: NF:audioclient.IAudioClock.GetPosition
title: IAudioClock::GetPosition (audioclient.h)
description: The GetPosition method gets the current device position.
helpviewer_keywords: ["GetPosition","GetPosition method [Core Audio]","GetPosition method [Core Audio]","IAudioClock interface","IAudioClock interface [Core Audio]","GetPosition method","IAudioClock.GetPosition","IAudioClock::GetPosition","IAudioClockGetPosition","audioclient/IAudioClock::GetPosition","coreaudio.iaudioclock_getposition"]
old-location: coreaudio\iaudioclock_getposition.htm
tech.root: CoreAudio
ms.assetid: 2271bd73-8cb6-4048-a16c-f765d0fae6bd
ms.date: 12/05/2018
ms.keywords: GetPosition, GetPosition method [Core Audio], GetPosition method [Core Audio],IAudioClock interface, IAudioClock interface [Core Audio],GetPosition method, IAudioClock.GetPosition, IAudioClock::GetPosition, IAudioClockGetPosition, audioclient/IAudioClock::GetPosition, coreaudio.iaudioclock_getposition
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioClock::GetPosition
 - audioclient/IAudioClock::GetPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClock.GetPosition
---

# IAudioClock::GetPosition


## -description

The <b>GetPosition</b> method gets the current device position.

## -parameters

### -param pu64Position [out]

Pointer to a <b>UINT64</b> variable into which the method writes the device position. The device position is the offset from the start of the stream to the current position in the stream. However, the units in which this offset is expressed are undefined—the device position value has meaning only in relation to the frequency reported by the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getfrequency">IAudioClock::GetFrequency</a> method. For more information, see Remarks.

### -param pu64QPCPosition [out]

Pointer to a <b>UINT64</b> variable into which the method writes the value of the performance counter at the time that the audio endpoint device read the device position (<i>*pu64Position</i>) in response to the <b>GetPosition</b> call. The method converts the counter value to 100-nanosecond time units before writing it to <i>*pu64QPCPosition</i>. This parameter can be <b>NULL</b> if the client does not require the performance counter value.

## -returns

If the method succeeds and obtains an accurate reading of the position, it returns S_OK. If the method succeeds but the duration of the call is long enough to detract from the accuracy of the position reading, the method returns S_FALSE. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Parameter <i>pu64Position</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>

## -remarks

Rendering or capture clients that need to expose a clock based on the stream's current playback or record position can use this method to derive that clock.

This method retrieves two correlated stream-position values:

<ul>
<li>Device position. The client obtains the device position through output parameter <i>pu64Position</i>. This is the stream position of the sample that is currently playing through the speakers (for a rendering stream) or being recorded through the microphone (for a capture stream).</li>
<li>Performance counter. The client obtains the performance counter through output parameter <i>pu64QPCPosition</i>. This is the counter value that the method obtained by calling the <b>QueryPerformanceCounter</b> function at the time that the audio endpoint device recorded the stream position (<i>*pu64Position</i>). Note that <b>GetPosition</b> converts the counter value to 100-nanosecond time units.</li>
</ul>
The device position is meaningless unless it is combined with the device frequency reported by the <b>IAudioClock::GetFrequency</b> method. The reason is that the units in which the device positions for different streams are expressed might vary according to factors such as whether the stream was opened in shared mode or exclusive mode. However, the frequency <i>f</i> obtained from <b>GetFrequency</b> is always expressed in units that are compatible with those of the device position <i>p</i>. Thus, the stream-relative offset in seconds can always be calculated as <i>p</i>/<i>f</i>.

The device position is a stream-relative offset. That is, it is specified as an offset from the start of the stream. The device position can be thought of as an offset into an idealized buffer that contains the entire stream and is contiguous from beginning to end.

Given the device position and the performance counter at the time of the <b>GetPosition</b> call, the client can provide a more timely estimate of the device position at a slightly later time by calling <b>QueryPerformanceCounter</b> to obtain the current performance counter, and extrapolating the device position based on how far the counter has advanced since the original device position was recorded. The client can call the <b>QueryPerformanceFrequency</b> function to determine the frequency of the clock that increments the counter. Before comparing the raw counter value obtained from <b>QueryPerformanceCounter</b> to the value written to <i>*pu64QPCPosition</i> by <b>GetPosition</b>, convert the raw counter value to 100-nanosecond time units as follows:

<ol>
<li>Multiply the raw counter value by 10,000,000.</li>
<li>Divide the result by the counter frequency obtained from <b>QueryPerformanceFrequency</b>.</li>
</ol>
For more information about <b>QueryPerformanceCounter</b> and <b>QueryPerformanceFrequency</b>, see the Windows SDK documentation.

Immediately following creation of a new stream, the device position is 0. Following a call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a> method, the device position increments at a uniform rate. The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">IAudioClient::Stop</a> method freezes the device position, and a subsequent <b>Start</b> call causes the device position to resume incrementing from its value at the time of the <b>Stop</b> call. A call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">IAudioClient::Reset</a>, which should only occur while the stream is stopped, resets the device position to 0.

When a new or reset rendering stream initially begins running, its device position might remain 0 for a few milliseconds until the audio data has had time to propagate from the endpoint buffer to the rendering endpoint device. The device position changes from 0 to a nonzero value when the data begins playing through the device.

Successive device readings are monotonically increasing. Although the device position might not change between two successive readings, the device position never decreases from one reading to the next.

The <i>pu64Position</i> parameter must be a valid, non-<b>NULL</b> pointer or the method will fail and return error code E_POINTER.

Position measurements might occasionally be delayed by intermittent, high-priority events. These events might be unrelated to audio. In the case of an exclusive-mode stream, the method can return S_FALSE instead of S_OK if the method succeeds but the duration of the call is long enough to detract from the accuracy of the reported position. When this occurs, the caller has the option of calling the method again to attempt to retrieve a more accurate position (as indicated by return value S_OK). However, the caller should avoid performing this test in an infinite loop in the event that the method consistently returns S_FALSE.

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">IAudioClient::Reset</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">IAudioClient::Stop</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclock-getfrequency">IAudioClock::GetFrequency</a>