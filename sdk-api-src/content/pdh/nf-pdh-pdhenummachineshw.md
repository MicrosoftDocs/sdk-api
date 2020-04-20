---
UID: NF:pdh.PdhEnumMachinesHW
title: PdhEnumMachinesHW function (pdh.h)
description: Returns a list of the computer names associated with counters in a log file.helpviewer_keywords: ["PdhEnumMachinesH","PdhEnumMachinesH function [Perf]","PdhEnumMachinesHA","PdhEnumMachinesHW","_win32_pdhenummachinesh","base.pdhenummachinesh","pdh/PdhEnumMachinesH","pdh/PdhEnumMachinesHA","pdh/PdhEnumMachinesHW","perf.pdhenummachinesh"]
old-location: perf\pdhenummachinesh.htm
tech.root: perfctrs
ms.assetid: 7e8dc113-76a7-4a7a-bbad-1a4387831501
ms.date: 12/05/2018
ms.keywords: PdhEnumMachinesH, PdhEnumMachinesH function [Perf], PdhEnumMachinesHA, PdhEnumMachinesHW, _win32_pdhenummachinesh, base.pdhenummachinesh, pdh/PdhEnumMachinesH, pdh/PdhEnumMachinesHA, pdh/PdhEnumMachinesHW, perf.pdhenummachinesh
f1_keywords:
- pdh/PdhEnumMachinesH
dev_langs:
- c++
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhEnumMachinesHW (Unicode) and PdhEnumMachinesHA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Pdh.dll
api_name:
- PdhEnumMachinesH
- PdhEnumMachinesHA
- PdhEnumMachinesHW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PdhEnumMachinesHW function


## -description


Returns a list of the computer names associated with counters in a log file. The computer names were either specified when adding counters to the query or when calling the <a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhconnectmachinea">PdhConnectMachine</a> function. The computers listed include those that are currently connected and online, in addition to those that are offline or not returning performance data.
			

This function is identical to 
the <a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhenummachinesa">PdhEnumMachines</a> function, except that it supports the use of handles to data sources.


## -parameters




### -param hDataSource [in]

Handle to a data source returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a> function.  




### -param mszMachineList [out]

Caller-allocated buffer to receive the list of <b>null</b>-terminated strings that contain the computer names. The list is terminated with two <b>null</b>-terminator characters. Set to <b>NULL</b> if <i>pcchBufferLength</i> is zero.


### -param pcchBufferSize [in, out]

Size of the <i>mszMachineNameList</i> buffer, in <b>TCHARs</b>. If zero on input, the function returns PDH_MORE_DATA and sets this parameter to the required buffer size. If the buffer is larger than the required size, the function sets this parameter to the actual size of the buffer that was used. If the specified size on input is greater than zero but less than the required size, you should not rely on the returned size to reallocate the buffer.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

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




<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhbindinputdatasourcea">PdhBindInputDataSource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/pdh/nf-pdh-pdhconnectmachinea">PdhConnectMachine</a>
 

 

