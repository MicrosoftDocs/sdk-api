---
UID: NF:endpointvolume.IAudioMeterInformation.GetPeakValue
title: IAudioMeterInformation::GetPeakValue
author: windows-sdk-content
description: The GetPeakValue method gets the peak sample value for the channels in the audio stream.
old-location: coreaudio\iaudiometerinformation_getpeakvalue.htm
old-project: CoreAudio
ms.assetid: 10abf43a-dfd8-4ced-893a-03f52ff4ee26
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetPeakValue, GetPeakValue method [Core Audio], GetPeakValue method [Core Audio],IAudioMeterInformation interface, IAudioMeterInformation interface [Core Audio],GetPeakValue method, IAudioMeterInformation.GetPeakValue, IAudioMeterInformation::GetPeakValue, IAudioMeterInformationGetPeakValue, coreaudio.iaudiometerinformation_getpeakvalue, endpointvolume/IAudioMeterInformation::GetPeakValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IAudioMeterInformation.GetPeakValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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



This method retrieves the peak sample value recorded across all of the channels in the stream. The peak value for each channel is recorded over one device period and made available during the subsequent device period. Thus, this method always retrieves the peak value recorded during the previous device period. To obtain the device period, call the <a href="https://msdn.microsoft.com/f2f75fce-9eca-488d-b183-87d97d4e599a">IAudioClient::GetDevicePeriod</a> method.

For a code example that uses the <b>GetPeakValue</b> method, see <a href="https://msdn.microsoft.com/02f5d1b4-ba4f-424a-897f-b113d1f7cd6b">Peak Meters</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2f75fce-9eca-488d-b183-87d97d4e599a">IAudioClient::GetDevicePeriod</a>



<a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation Interface</a>
 

 

