---
UID: NF:pdh.PdhEnumMachinesA
title: PdhEnumMachinesA function
author: windows-driver-content
description: Returns a list of the computer names associated with counters in a log file.
old-location: perf\pdhenummachines.htm
old-project: PerfCtrs
ms.assetid: 77584d3b-3ba5-4288-b730-be2458f4fc1c
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PdhEnumMachines, PdhEnumMachines function [Perf], PdhEnumMachinesA, PdhEnumMachinesW, _win32_pdhenummachines, base.pdhenummachines, pdh/PdhEnumMachines, pdh/PdhEnumMachinesA, pdh/PdhEnumMachinesW, perf.pdhenummachines
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
req.unicode-ansi: PdhEnumMachinesW (Unicode) and PdhEnumMachinesA (ANSI)
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
-	PdhEnumMachines
-	PdhEnumMachinesA
-	PdhEnumMachinesW
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PdhEnumMachinesA function


## -description


Returns a list of the computer names associated with counters in a log file. The computer names were either specified when adding counters to the query or when calling the <a href="https://msdn.microsoft.com/8f8b4651-b550-4b34-bb2f-d2497c56b572">PdhConnectMachine</a> function. The computers listed include those that are currently connected and online, in addition to those that are offline or not returning performance data.
			

To use handles to data sources, use the 
<a href="https://msdn.microsoft.com/7e8dc113-76a7-4a7a-bbad-1a4387831501">PdhEnumMachinesH</a> function.


## -parameters




### -param szDataSource [in]

<b>Null</b>-terminated string that specifies the name of a log file. The function enumerates the names of the computers whose counter data is in the log file. If <b>NULL</b>, the function enumerates the list of computers that were specified when adding counters to a real time query or when calling the <a href="https://msdn.microsoft.com/8f8b4651-b550-4b34-bb2f-d2497c56b572">PdhConnectMachine</a> function.


### -param mszMachineList

TBD


### -param pcchBufferSize

TBD




#### - mszMachineNameList [out]

Caller-allocated buffer to receive the list of <b>null</b>-terminated strings that contain the computer names. The list is terminated with two <b>null</b>-terminator characters. Set to <b>NULL</b> if <i>pcchBufferLength</i> is zero.


#### - pcchBufferLength [in, out]

Size of the <i>mszMachineNameList</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.


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
<dt><b>PDH_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>mszMachineNameList</i> buffer is too small to contain all the data. This return value is expected if <i>pcchBufferLength</i> is zero on input. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not valid. For example, on some releases you could receive this error if the specified size on input is greater than zero but less than the required size.

</td>
</tr>
</table>
 




## -remarks



You should call this function twice, the first time to get the required buffer size (set <i>mszMachineNameList</i> to <b>NULL</b> and <i>pcchBufferLength</i> to 0), and the second time to get the data.




## -see-also




<a href="https://msdn.microsoft.com/8f8b4651-b550-4b34-bb2f-d2497c56b572">PdhConnectMachine</a>



<a href="https://msdn.microsoft.com/7e8dc113-76a7-4a7a-bbad-1a4387831501">PdhEnumMachinesH</a>
 

 

