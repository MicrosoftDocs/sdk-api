---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

