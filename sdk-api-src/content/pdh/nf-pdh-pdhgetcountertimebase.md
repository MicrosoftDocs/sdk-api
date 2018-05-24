---
UID: NF:pdh.PdhGetCounterTimeBase
title: PdhGetCounterTimeBase function
author: windows-driver-content
description: Returns the time base of the specified counter.
old-location: perf\pdhgetcountertimebase.htm
old-project: PerfCtrs
ms.assetid: b034c00e-50f1-46af-aebc-0cb968c0b737
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PdhGetCounterTimeBase, PdhGetCounterTimeBase function [Perf], _win32_pdhgetcountertimebase, base.pdhgetcountertimebase, pdh/PdhGetCounterTimeBase, perf.pdhgetcountertimebase
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
-	PdhGetCounterTimeBase
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PdhGetCounterTimeBase function


## -description


Returns the time base of the specified counter.
		


## -parameters




### -param hCounter [in]

Handle to the counter. The 
<a href="https://msdn.microsoft.com/b8b9a332-ce28-46d4-92e2-91f9f6c24da5">PdhAddCounter</a> function returns this handle.


### -param pTimeBase [out]

Time base that specifies the number of performance values a counter samples per second.


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
The specified counter does not use a time base.

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
 




## -remarks



If you use 
			the 
<a href="https://msdn.microsoft.com/13027af4-2e76-4c2f-88e8-a2554a16fae3">PdhFormatFromRawValue</a> function to calculate a displayable value instead of calling the <a href="https://msdn.microsoft.com/fd50b1fd-29b7-49a8-bbcc-4d7f0cbd7079">PdhCalculateCounterFromRawValue</a> function, you must call the 
<b>PdhGetCounterTimeBase</b> function to retrieve the time base.
		

Each counter that returns time-based performance data has a time base defined for it. The time base of a counter is the number of times a counter samples data per second. 




## -see-also




<a href="https://msdn.microsoft.com/13027af4-2e76-4c2f-88e8-a2554a16fae3">PdhFormatFromRawValue</a>
 

 

