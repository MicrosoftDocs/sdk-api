---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetSamplingRate
title: IIsdbAudioComponentDescriptor::GetSamplingRate
author: windows-sdk-content
description: Gets the value of the sampling_rate field from a an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This three-bit field contains a code that indicates the sampling frequency.
old-location: mstv\iisdbaudiocomponentdescriptor_getsamplingrate.htm
tech.root: mstv
ms.assetid: ccb31b56-10a1-47ee-9d1b-116d860bef11
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSamplingRate, GetSamplingRate method [Microsoft TV Technologies], GetSamplingRate method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetSamplingRate method, IIsdbAudioComponentDescriptor.GetSamplingRate, IIsdbAudioComponentDescriptor::GetSamplingRate, dvbsiparser/IIsdbAudioComponentDescriptor::GetSamplingRate, mstv.iisdbaudiocomponentdescriptor_getsamplingrate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - dvbsiparser.h
api_name:
 - IIsdbAudioComponentDescriptor.GetSamplingRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbAudioComponentDescriptor::GetSamplingRate


## -description


 Gets the value of the sampling_rate field from a an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This three-bit field contains a code that indicates the sampling frequency.


## -parameters




### -param pbVal [out]

Receives one of the following codes:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>000</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>001</dt>
</dl>
</td>
<td width="60%">
16 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>010</dt>
</dl>
</td>
<td width="60%">
22.05 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>011</dt>
</dl>
</td>
<td width="60%">
24 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>101</dt>
</dl>
</td>
<td width="60%">
32 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>110</dt>
</dl>
</td>
<td width="60%">
44.1 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>111</dt>
</dl>
</td>
<td width="60%">
48 kHz.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f771b318-5fd5-4c7f-a22b-6966aec5c0fa">IIsdbAudioComponentDescriptor</a>
 

 

