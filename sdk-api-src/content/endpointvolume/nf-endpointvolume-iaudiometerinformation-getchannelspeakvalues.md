---
UID: NF:endpointvolume.IAudioMeterInformation.GetChannelsPeakValues
title: IAudioMeterInformation::GetChannelsPeakValues method
author: windows-driver-content
description: The GetChannelsPeakValues method gets the peak sample values for all the channels in the audio stream.
old-location: coreaudio\iaudiometerinformation_getchannelspeakvalues.htm
old-project: CoreAudio
ms.assetid: f5caf927-50c4-48dc-b396-016a1cf88882
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: GetChannelsPeakValues method [Core Audio], GetChannelsPeakValues method [Core Audio], IAudioMeterInformation interface, GetChannelsPeakValues,IAudioMeterInformation.GetChannelsPeakValues, IAudioMeterInformation, IAudioMeterInformation interface [Core Audio], GetChannelsPeakValues method, IAudioMeterInformation::GetChannelsPeakValues, IAudioMeterInformationGetChannelsPeakValues, coreaudio.iaudiometerinformation_getchannelspeakvalues, endpointvolume/IAudioMeterInformation::GetChannelsPeakValues
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Endpointvolume.h
api_name:
-	IAudioMeterInformation.GetChannelsPeakValues
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioMeterInformation::GetChannelsPeakValues method


## -description



The <b>GetChannelsPeakValues</b> method gets the peak sample values for all the channels in the audio stream.




## -parameters




### -param u32ChannelCount [in]

The channel count. This parameter also specifies the number of elements in the <i>afPeakValues</i> array. If the specified count does not match the number of channels in the stream, the method returns error code E_INVALIDARG.


### -param afPeakValues [out]

Pointer to an array of peak sample values. The method writes the peak values for the channels into the array. The array contains one element for each channel in the stream. The peak values are numbers in the normalized range from 0.0 to 1.0.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>u32ChannelCount</i> does not equal the number of channels in the audio stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>afPeakValues</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method retrieves the peak sample values for the channels in the stream. The peak value for each channel is recorded over one device period and made available during the subsequent device period. Thus, this method always retrieves the peak values recorded during the previous device period. To obtain the device period, call the <a href="https://msdn.microsoft.com/f2f75fce-9eca-488d-b183-87d97d4e599a">IAudioClient::GetDevicePeriod</a> method.

Parameter <i>afPeakValues</i> points to a caller-allocated <b>float</b> array. If the stream contains <i>n</i> channels, the channels are numbered 0 to <i>n</i>– 1. The method stores the peak value for each channel in the array element whose array index matches the channel number. To get the number of channels in the audio stream that are monitored by peak meters, call the <a href="https://msdn.microsoft.com/6f1deef6-cc47-4736-b0bb-99afb1966895">IAudioMeterInformation::GetMeteringChannelCount</a> method.




## -see-also




<a href="https://msdn.microsoft.com/f2f75fce-9eca-488d-b183-87d97d4e599a">IAudioClient::GetDevicePeriod</a>



<a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation Interface</a>



<a href="https://msdn.microsoft.com/6f1deef6-cc47-4736-b0bb-99afb1966895">IAudioMeterInformation::GetMeteringChannelCount</a>
 

 

