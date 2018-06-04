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

# SetProcessShutdownParameters function


## -description


Sets shutdown parameters for the currently calling process. This function sets a shutdown order for a process relative to the other processes in the system.


## -parameters




### -param dwLevel [in]

The shutdown priority for a process relative to other processes in the system. The system shuts down processes from high <i>dwLevel</i> values to low. The highest and lowest shutdown priorities are reserved for system components. This parameter must be in the following range of values. 



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


### -param dwFlags [in]

This parameter can be the following value.

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
The system terminates the process without displaying a retry dialog box for the user.

</td>
</tr>
</table>
 


## -returns



If the function is succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications running in the system security context do not get shut down by the operating system. They get notified of shutdown or logoff through the callback function installable via 
<a href="base.setconsolectrlhandler">SetConsoleCtrlHandler</a>. They also get notified in the order specified by the <i>dwLevel</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/68b48e67-c7e0-4434-bef5-b2aaebb343ff">GetProcessShutdownParameters</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="base.setconsolectrlhandler">SetConsoleCtrlHandler</a>
 

 

