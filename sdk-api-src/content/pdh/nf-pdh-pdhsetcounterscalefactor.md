---
UID: NF:pdh.PdhSetCounterScaleFactor
title: PdhSetCounterScaleFactor function
author: windows-driver-content
description: Sets the scale factor that is applied to the calculated value of the specified counter when you request the formatted counter value. If the PDH_FMT_NOSCALE flag is set, then this scale factor is ignored.
old-location: perf\pdhsetcounterscalefactor.htm
old-project: PerfCtrs
ms.assetid: 6db99e03-0b03-4c1c-b82a-2982b52746db
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: PdhSetCounterScaleFactor, PdhSetCounterScaleFactor function [Perf], _win32_pdhsetcounterscalefactor, base.pdhsetcounterscalefactor, pdh/PdhSetCounterScaleFactor, perf.pdhsetcounterscalefactor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhSetCounterScaleFactor
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PdhSetCounterScaleFactor function


## -description



			Sets the scale factor that is applied to the calculated value of the specified counter when you request the formatted counter value. If the PDH_FMT_NOSCALE flag is set, then this scale factor is ignored.
		


## -parameters




### -param hCounter [in]

Handle of the counter to apply the scale factor to. The 
<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function returns this handle.


### -param lFactor [in]

Power of ten by which to multiply the calculated value before returning it. The minimum value of this parameter is PDH_MIN_SCALE (–7), where the returned value is the actual value multiplied by 10<sup>–</sup>⁷. The maximum value of this parameter is PDH_MAX_SCALE (+7), where the returned value is the actual value multiplied by 10⁺⁷. A value of zero will set the scale to one, so that the actual value is returned.


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The scale value is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The counter handle is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a>



<a href="https://msdn.microsoft.com/a986ae6c-88ee-4a03-9077-3d286157b9d1">PdhComputeCounterStatistics</a>



<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>
 

 

