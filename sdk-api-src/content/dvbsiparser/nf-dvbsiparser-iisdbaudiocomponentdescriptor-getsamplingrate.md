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
 

 

