---
UID: NF:endpointvolume.IAudioMeterInformation.GetPeakValue
title: IAudioMeterInformation::GetPeakValue (endpointvolume.h)
description: The GetPeakValue method gets the peak sample value for the channels in the audio stream.
helpviewer_keywords: ["GetPeakValue","GetPeakValue method [Core Audio]","GetPeakValue method [Core Audio]","IAudioMeterInformation interface","IAudioMeterInformation interface [Core Audio]","GetPeakValue method","IAudioMeterInformation.GetPeakValue","IAudioMeterInformation::GetPeakValue","IAudioMeterInformationGetPeakValue","coreaudio.iaudiometerinformation_getpeakvalue","endpointvolume/IAudioMeterInformation::GetPeakValue"]
old-location: coreaudio\iaudiometerinformation_getpeakvalue.htm
tech.root: CoreAudio
ms.assetid: 10abf43a-dfd8-4ced-893a-03f52ff4ee26
ms.date: 12/05/2018
ms.keywords: GetPeakValue, GetPeakValue method [Core Audio], GetPeakValue method [Core Audio],IAudioMeterInformation interface, IAudioMeterInformation interface [Core Audio],GetPeakValue method, IAudioMeterInformation.GetPeakValue, IAudioMeterInformation::GetPeakValue, IAudioMeterInformationGetPeakValue, coreaudio.iaudiometerinformation_getpeakvalue, endpointvolume/IAudioMeterInformation::GetPeakValue
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
 - IAudioMeterInformation::GetPeakValue
 - endpointvolume/IAudioMeterInformation::GetPeakValue
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
 - IAudioMeterInformation.GetPeakValue
---

# IAudioMeterInformation::GetPeakValue


## -description

The <b>GetPeakValue</b> method gets the peak sample value for the channels in the audio stream.

## -parameters

### -param pfPeak [out]

Pointer to a <b>float</b> variable into which the method writes the peak sample value for the audio stream. The peak value is a number in the normalized range from 0.0 to 1.0.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfPeak</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method retrieves the peak sample value recorded across all of the channels in the stream. The peak value for each channel is recorded over one device period and made available during the subsequent device period. Thus, this method always retrieves the peak value recorded during the previous device period. To obtain the device period, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getdeviceperiod">IAudioClient::GetDevicePeriod</a> method.

For a code example that uses the <b>GetPeakValue</b> method, see <a href="/windows/desktop/CoreAudio/peak-meters">Peak Meters</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getdeviceperiod">IAudioClient::GetDevicePeriod</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudiometerinformation">IAudioMeterInformation Interface</a>