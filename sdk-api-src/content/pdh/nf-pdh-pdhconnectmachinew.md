---
UID: NF:pdh.PdhConnectMachineW
title: PdhConnectMachineW function (pdh.h)
author: windows-sdk-content
description: Connects to the specified computer.
old-location: perf\pdhconnectmachine.htm
tech.root: perfctrs
ms.assetid: 8f8b4651-b550-4b34-bb2f-d2497c56b572
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PdhConnectMachine, PdhConnectMachine function [Perf], PdhConnectMachineA, PdhConnectMachineW, _win32_pdhconnectmachine, base.pdhconnectmachine, pdh/PdhConnectMachine, pdh/PdhConnectMachineA, pdh/PdhConnectMachineW, perf.pdhconnectmachine
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

However, you can use this function if you want to include more than the local computer in the <b>Select counters from computer</b> list on the <b>Browse Counters</b> dialog box. For details, see the <a href="https://msdn.microsoft.com/8e045e0b-c157-4527-902c-6096c7922642">PDH_BROWSE_DLG_CONFIG</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/77584d3b-3ba5-4288-b730-be2458f4fc1c">PdhEnumMachines</a>
 

 

