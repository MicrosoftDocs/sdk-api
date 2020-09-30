---
UID: NF:endpointvolume.IAudioMeterInformation.GetChannelsPeakValues
title: IAudioMeterInformation::GetChannelsPeakValues (endpointvolume.h)
description: The GetChannelsPeakValues method gets the peak sample values for all the channels in the audio stream.
helpviewer_keywords: ["GetChannelsPeakValues","GetChannelsPeakValues method [Core Audio]","GetChannelsPeakValues method [Core Audio]","IAudioMeterInformation interface","IAudioMeterInformation interface [Core Audio]","GetChannelsPeakValues method","IAudioMeterInformation.GetChannelsPeakValues","IAudioMeterInformation::GetChannelsPeakValues","IAudioMeterInformationGetChannelsPeakValues","coreaudio.iaudiometerinformation_getchannelspeakvalues","endpointvolume/IAudioMeterInformation::GetChannelsPeakValues"]
old-location: coreaudio\iaudiometerinformation_getchannelspeakvalues.htm
tech.root: CoreAudio
ms.assetid: f5caf927-50c4-48dc-b396-016a1cf88882
ms.date: 12/05/2018
ms.keywords: GetChannelsPeakValues, GetChannelsPeakValues method [Core Audio], GetChannelsPeakValues method [Core Audio],IAudioMeterInformation interface, IAudioMeterInformation interface [Core Audio],GetChannelsPeakValues method, IAudioMeterInformation.GetChannelsPeakValues, IAudioMeterInformation::GetChannelsPeakValues, IAudioMeterInformationGetChannelsPeakValues, coreaudio.iaudiometerinformation_getchannelspeakvalues, endpointvolume/IAudioMeterInformation::GetChannelsPeakValues
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioMeterInformation::GetChannelsPeakValues
 - endpointvolume/IAudioMeterInformation::GetChannelsPeakValues
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioMeterInformation.GetChannelsPeakValues
---

# IAudioMeterInformation::GetChannelsPeakValues


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

This method retrieves the peak sample values for the channels in the stream. The peak value for each channel is recorded over one device period and made available during the subsequent device period. Thus, this method always retrieves the peak values recorded during the previous device period. To obtain the device period, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getdeviceperiod">IAudioClient::GetDevicePeriod</a> method.

Parameter <i>afPeakValues</i> points to a caller-allocated <b>float</b> array. If the stream contains <i>n</i> channels, the channels are numbered 0 to <i>n</i>– 1. The method stores the peak value for each channel in the array element whose array index matches the channel number. To get the number of channels in the audio stream that are monitored by peak meters, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-getmeteringchannelcount">IAudioMeterInformation::GetMeteringChannelCount</a> method.

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getdeviceperiod">IAudioClient::GetDevicePeriod</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudiometerinformation">IAudioMeterInformation Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudiometerinformation-getmeteringchannelcount">IAudioMeterInformation::GetMeteringChannelCount</a>