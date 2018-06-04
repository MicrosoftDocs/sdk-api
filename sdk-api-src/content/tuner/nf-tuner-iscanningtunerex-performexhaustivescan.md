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

# IScanningTunerEx::PerformExhaustiveScan


## -description



This topic applies to Windows Vista and later.
        



The <b>PerformExhaustiveScan</b> method scans a range of frequencies until the tuner locks onto a signal.


## -parameters




### -param dwLowerFreq [in]

Lowest frequency in the range of frequencies to scan. A value of -1 specifies the minimum frequency as determined by the device.


### -param dwHigherFreq [in]

Highest frequency in the range of frequencies to scan. A value of -1 specifies the maximum frequency as determined by the device.


### -param bFineTune [in]

Specifies whether the tuner performs fine tuning. When the tuner locks onto a frequency, if this parameter is <b>VARIANT_TRUE</b>, the tuner does fine tuning to find the best possible signal around that frequency.


### -param hEvent [in]

Handle to an event created by the application. When the tuner locks onto a signal, it signals this event.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
No scan is currently in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
Invalid frequency argument (for example, 0 <i>dwLowerFrequency</i> or <i>dwHigherFreq</i> value or <i>dwLowerFrequency</i> &gt;= <i>dwHigherFreq</i>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

