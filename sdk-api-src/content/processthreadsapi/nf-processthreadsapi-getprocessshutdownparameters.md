---
UID: NF:processthreadsapi.GetProcessShutdownParameters
title: GetProcessShutdownParameters function
author: windows-sdk-content
description: Retrieves the shutdown parameters for the currently calling process.
old-location: base\getprocessshutdownparameters.htm
tech.root: procthread
ms.assetid: 68b48e67-c7e0-4434-bef5-b2aaebb343ff
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetProcessShutdownParameters, GetProcessShutdownParameters function, SHUTDOWN_NORETRY, _win32_getprocessshutdownparameters, base.getprocessshutdownparameters, processthreadsapi/GetProcessShutdownParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-Ms-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
api_name:
 - GetProcessShutdownParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetProcessShutdownParameters function


## -description


Retrieves the shutdown parameters for the currently calling process.


## -parameters




### -param lpdwLevel [out]

A pointer to a variable that receives the shutdown priority level. Higher levels shut down first. System level shutdown orders are reserved for system components. Higher numbers shut down first. Following are the level conventions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>000-0FF</dt>
</dl>
</td>
<td width="60%">
System reserved last shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>100-1FF</dt>
</dl>
</td>
<td width="60%">
Application reserved last shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>200-2FF</dt>
</dl>
</td>
<td width="60%">
Application reserved "in between" shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>300-3FF</dt>
</dl>
</td>
<td width="60%">
Application reserved first shutdown range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>400-4FF</dt>
</dl>
</td>
<td width="60%">
System reserved first shutdown range.

</td>
</tr>
</table>
 

All processes start at shutdown level 0x280.


### -param lpdwFlags [out]

A pointer to a variable that receives the shutdown flags. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SHUTDOWN_NORETRY"></a><a id="shutdown_noretry"></a><dl>
<dt><b>SHUTDOWN_NORETRY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this process takes longer than the specified timeout to shut down, do not display a retry dialog box for the user. Instead, just cause the process to directly exit.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/c467950e-31e1-4608-a08a-0736a5524e0e">SetProcessShutdownParameters</a>
 

 

