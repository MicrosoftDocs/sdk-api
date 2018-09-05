---
UID: NN:endpointvolume.IAudioMeterInformation
title: IAudioMeterInformation
author: windows-sdk-content
description: The IAudioMeterInformation interface represents a peak meter on an audio stream to or from an audio endpoint device.
old-location: coreaudio\iaudiometerinformation.htm
old-project: CoreAudio
ms.assetid: eff1c1cd-792b-489a-8381-4b783c57f005
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioMeterInformation, IAudioMeterInformation interface [Core Audio], IAudioMeterInformation interface [Core Audio],described, coreaudio.iaudiometerinformation, endpointvolume/IAudioMeterInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: endpointvolume.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ProtType
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioMeterInformation interface


## -description



The <b>IAudioMeterInformation</b> interface represents a peak meter on an audio stream to or from an audio endpoint device. The client obtains a reference to the <b>IAudioMeterInformation</b> interface on an endpoint object by calling the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioMeterInformation.

If the adapter device that streams audio data to or from the endpoint device implements a hardware peak meter, the <b>IAudioMeterInformation</b> interface uses that meter to monitor the peak levels in the audio stream. If the audio device lacks a hardware peak meter, the audio engine automatically implements the peak meter in software, transparently to the client.

If a device has a hardware peak meter, a client can use the methods in the <b>IAudioMeterInformation</b> interface to monitor the device's peak levels in both shared mode and exclusive mode. If a device lacks a hardware peak meter, a client can use those methods to monitor the device's peak levels in shared mode, but not in exclusive mode. In exclusive mode, the client and the device exchange audio data directly, bypassing the software peak meter. In exclusive mode, a software peak meter always reports a peak value of 0.0.

To determine whether a device has a hardware peak meter, call the <a href="https://msdn.microsoft.com/3f68a459-8c10-46f5-be5c-67b693d65b8b">IAudioMeterInformation::QueryHardwareSupport</a> method.

For a rendering endpoint device, the <b>IAudioMeterInformation</b> interface monitors the peak levels in the output stream before the stream is attenuated by the endpoint volume controls. Similarly, for a capture endpoint device, the interface monitors the peak levels in the input stream before the stream is attenuated by the endpoint volume controls.

The peak values reported by the methods in the <b>IAudioMeterInformation</b> interface are normalized to the range from 0.0 to 1.0. For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is –8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the <b>IAudioMeterInformation</b> interface is 8914/32768 = 0.272.

For a code example that uses the <b>IAudioMeterInformation</b> interface, see <a href="https://msdn.microsoft.com/02f5d1b4-ba4f-424a-897f-b113d1f7cd6b">Peak Meters</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioMeterInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioMeterInformation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f5caf927-50c4-48dc-b396-016a1cf88882">GetChannelsPeakValues</a>
</td>
<td align="left" width="63%">
Gets the peak sample values for all the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f1deef6-cc47-4736-b0bb-99afb1966895">GetMeteringChannelCount</a>
</td>
<td align="left" width="63%">
Gets the number of channels in the audio stream that are monitored by peak meters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10abf43a-dfd8-4ced-893a-03f52ff4ee26">GetPeakValue</a>
</td>
<td align="left" width="63%">
Gets the peak sample value for the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f68a459-8c10-46f5-be5c-67b693d65b8b">QueryHardwareSupport</a>
</td>
<td align="left" width="63%">
Queries the audio endpoint device for its hardware-supported functions.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79">EndpointVolume API</a>



<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>
 

 

