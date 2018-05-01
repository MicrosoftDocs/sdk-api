---
UID: NF:tuner.IScanningTunerEx.PerformExhaustiveScan
title: IScanningTunerEx::PerformExhaustiveScan method
author: windows-driver-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_performexhaustivescan.htm
old-project: mstv
ms.assetid: 35ed1b43-020e-4baa-9f15-eb316d9a137b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IScanningTunerEx, IScanningTunerEx interface [Microsoft TV Technologies], PerformExhaustiveScan method, IScanningTunerEx::PerformExhaustiveScan, IScanningTunerExPerformExhaustiveScan, PerformExhaustiveScan method [Microsoft TV Technologies], PerformExhaustiveScan method [Microsoft TV Technologies], IScanningTunerEx interface, PerformExhaustiveScan,IScanningTunerEx.PerformExhaustiveScan, mstv.iscanningtunerex_performexhaustivescan, tuner/IScanningTunerEx::PerformExhaustiveScan
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tuner.h
api_name:
-	IScanningTunerEx.PerformExhaustiveScan
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTunerEx::PerformExhaustiveScan method


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
 

 

