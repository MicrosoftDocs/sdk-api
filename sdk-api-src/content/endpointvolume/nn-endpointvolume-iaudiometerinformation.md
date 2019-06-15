---
UID: NN:endpointvolume.IAudioMeterInformation
title: IAudioMeterInformation (endpointvolume.h)
author: windows-sdk-content
description: The IAudioMeterInformation interface represents a peak meter on an audio stream to or from an audio endpoint device.
old-location: coreaudio\iaudiometerinformation.htm
tech.root: CoreAudio
ms.assetid: eff1c1cd-792b-489a-8381-4b783c57f005
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioMeterInformation, IAudioMeterInformation interface [Core Audio], IAudioMeterInformation interface [Core Audio],described, coreaudio.iaudiometerinformation, endpointvolume/IAudioMeterInformation
ms.topic: interface
f1_keywords: ["endpointvolume/IAudioMeterInformation"]
req.header: endpointvolume.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioMeterInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioMeterInformation interface


## -description



The <b>IAudioMeterInformation</b> interface represents a peak meter on an audio stream to or from an audio endpoint device. The client obtains a reference to the <b>IAudioMeterInformation</b> interface on an endpoint object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioMeterInformation.

If the adapter device that streams audio data to or from the endpoint device implements a hardware peak meter, the <b>IAudioMeterInformation</b> interface uses that meter to monitor the peak levels in the audio stream. If the audio device lacks a hardware peak meter, the audio engine automatically implements the peak meter in software, transparently to the client.

If a device has a hardware peak meter, a client can use the methods in the <b>IAudioMeterInformation</b> interface to monitor the device's peak levels in both shared mode and exclusive mode. If a device lacks a hardware peak meter, a client can use those methods to monitor the device's peak levels in shared mode, but not in exclusive mode. In exclusive mode, the client and the device exchange audio data directly, bypassing the software peak meter. In exclusive mode, a software peak meter always reports a peak value of 0.0.

To determine whether a device has a hardware peak meter, call the <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport">IAudioMeterInformation::QueryHardwareSupport</a> method.

For a rendering endpoint device, the <b>IAudioMeterInformation</b> interface monitors the peak levels in the output stream before the stream is attenuated by the endpoint volume controls. Similarly, for a capture endpoint device, the interface monitors the peak levels in the input stream before the stream is attenuated by the endpoint volume controls.

The peak values reported by the methods in the <b>IAudioMeterInformation</b> interface are normalized to the range from 0.0 to 1.0. For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is –8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the <b>IAudioMeterInformation</b> interface is 8914/32768 = 0.272.

For a code example that uses the <b>IAudioMeterInformation</b> interface, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/peak-meters">Peak Meters</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioMeterInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioMeterInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioMeterInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-getchannelspeakvalues">GetChannelsPeakValues</a>
</td>
<td align="left" width="63%">
Gets the peak sample values for all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-getmeteringchannelcount">GetMeteringChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels in the audio stream that are monitored by peak meters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue">GetPeakValue</a>
</td>
<td align="left" width="63%">
Gets the peak sample value for the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport">QueryHardwareSupport</a>
</td>
<td align="left" width="63%">
Queries the audio endpoint device for its hardware-supported functions.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>
 

 

