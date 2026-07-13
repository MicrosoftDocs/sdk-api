---
UID: NF:pdh.PdhConnectMachineW
title: PdhConnectMachineW function (pdh.h)
description: Connects to the specified computer. (Unicode)
helpviewer_keywords: ["PdhConnectMachine", "PdhConnectMachine function [Perf]", "PdhConnectMachineW", "_win32_pdhconnectmachine", "base.pdhconnectmachine", "pdh/PdhConnectMachine", "pdh/PdhConnectMachineW", "perf.pdhconnectmachine"]
old-location: perf\pdhconnectmachine.htm
tech.root: perf
ms.assetid: 8f8b4651-b550-4b34-bb2f-d2497c56b572
ms.date: 12/05/2018
ms.keywords: PdhConnectMachine, PdhConnectMachine function [Perf], PdhConnectMachineA, PdhConnectMachineW, _win32_pdhconnectmachine, base.pdhconnectmachine, pdh/PdhConnectMachine, pdh/PdhConnectMachineA, pdh/PdhConnectMachineW, perf.pdhconnectmachine
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PdhConnectMachineW (Unicode) and PdhConnectMachineA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhConnectMachineW
 - pdh/PdhConnectMachineW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Pdh.dll
api_name:
 - PdhConnectMachine
 - PdhConnectMachineA
 - PdhConnectMachineW
---

# PdhConnectMachineW function


## -description

Connects to the specified computer.

## -parameters

### -param szMachineName [in]

<b>Null</b>-terminated string that specifies the name of the computer to connect to. If <b>NULL</b>, PDH connects to the local computer.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_CSTATUS_NO_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the specified computer. Could be caused by the computer not being on, not supporting PDH, not being connected to the network, or having the permissions set on the registry that prevent remote connections or remote performance monitoring by the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_MEMORY_ALLOCATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate a dynamic memory block. Occurs when there is a serious memory shortage in the system due to too many applications running on the system or an insufficient memory paging file.

</td>
</tr>
</table>

## -remarks

Typically, applications do not call this function and instead the connection is made when the application adds the counter to the query.

However, you can use this function if you want to include more than the local computer in the <b>Select counters from computer</b> list on the <b>Browse Counters</b> dialog box. For details, see the <a href="/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a">PDH_BROWSE_DLG_CONFIG</a> structure.





> [!NOTE]
> The pdh.h header defines PdhConnectMachine as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhenummachinesa">PdhEnumMachines</a>
