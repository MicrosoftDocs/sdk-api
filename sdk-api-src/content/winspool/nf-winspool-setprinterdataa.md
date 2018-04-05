---
UID: NF:winspool.SetPrinterDataA
title: SetPrinterDataA function
author: windows-driver-content
description: The SetPrinterData function sets the configuration data for a printer or print server.
old-location: gdi\setprinterdata.htm
old-project: printdocs
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetPrinterData, SetPrinterData function [Windows GDI], SetPrinterDataA, SetPrinterDataW, _win32_SetPrinterData, gdi.setprinterdata, winspool/SetPrinterData, winspool/SetPrinterDataA, winspool/SetPrinterDataW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetPrinterDataW (Unicode) and SetPrinterDataA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winspool.drv
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	SetPrinterData
-	SetPrinterDataA
-	SetPrinterDataW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetPrinterDataA function


## -description


The <b>SetPrinterData</b> function sets the configuration data for a printer or print server.

To specify the registry key under which to store the data, call the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> function. Calling <b>SetPrinterData</b> is equivalent to calling the <b>SetPrinterDataEx</b> function with the <i>pKeyName</i> parameter set to "PrinterDriverData".


## -parameters




### -param hPrinter [in]

A handle to the printer or print server for which the function sets configuration data. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>, <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>, or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pValueName [in]

A pointer to a null-terminated string that identifies the data to set.

For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.

For print servers, this string is one of the predefined strings listed in the following Remarks section.


### -param Type [in]

A code that indicates the type of data that the <i>pData</i> parameter points to. For a list of the possible type codes, see <a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.


### -param pData [in]

A pointer to an array of bytes that contains the printer configuration data.


### -param cbData [in]

The size, in bytes, of the array.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error value.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
To retrieve existing configuration data for a printer, call the <a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a> or <a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a> function.

If <i>hPrinter</i> is a handle to a print server, <i>pValueName</i> can specify one of the following predefined values.

<table>
<tr>
<th>Value</th>
<th>Comments</th>
</tr>
<tr>
<td><b>SPLREG_ALLOW_USER_MANAGEFORMS</b></td>
<td>
Windows XP with Service Pack 2 (SP2) and later

Windows Server 2003 with Service Pack 1 (SP1) and later

</td>
</tr>
<tr>
<td><b>SPLREG_BEEP_ENABLED</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_DEFAULT_SPOOL_DIRECTORY</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_EVENT_LOG</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_NET_POPUP</b></td>
<td>
Not supported in Windows Server 2003 and later

</td>
</tr>
<tr>
<td><b>SPLREG_PORT_THREAD_PRIORITY_DEFAULT</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_PORT_THREAD_PRIORITY</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_PRINT_DRIVER_ISOLATION_GROUPS</b></td>
<td>
Windows 7 and later

</td>
</tr>
<tr>
<td><b>SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE</b></td>
<td>
Windows 7 and later

</td>
</tr>
<tr>
<td><b>SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE</b></td>
<td>
Windows 7 and later

</td>
</tr>
<tr>
<td><b>SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT</b></td>
<td>
Windows 7 and later

</td>
</tr>
<tr>
<td><b>SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY</b></td>
<td>
Windows 7 and later

</td>
</tr>
<tr>
<td><b>SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY</b></td>
<td>
Windows 7 and later

</td>
</tr>
<tr>
<td><b>SPLREG_RETRY_POPUP</b></td>
<td>
On successful return, <i>pData</i> contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.

Not supported in Windows Server 2003 and later

</td>
</tr>
<tr>
<td><b>SPLREG_SCHEDULER_THREAD_PRIORITY</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_WEBSHAREMGMT</b></td>
<td>
Windows Server 2003 and later

</td>
</tr>
</table>
 

The following values of <i>pValueName</i> determine the pool printing behavior when an error occurs.

<table>
<tr>
<th>Value</th>
<th>Comments</th>
</tr>
<tr>
<td><b>SPLREG_RESTART_JOB_ON_POOL_ERROR</b></td>
<td>
The value of <i>pData</i> indicates the time, in seconds, when a job is restarted on another port after an error occurs. This setting is used with <b>SPLREG_RESTART_JOB_ON_POOL_ENABLED</b>.

</td>
</tr>
<tr>
<td><b>SPLREG_RESTART_JOB_ON_POOL_ENABLED</b></td>
<td>
A nonzero value in <i>pData</i> indicates that <b>SPLREG_RESTART_JOB_ON_POOL_ERROR</b> is enabled.

</td>
</tr>
</table>
 

The time specified in <b>SPLREG_RESTART_JOB_ON_POOL_ERROR</b> is a minimum time. The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:


<b>HKLM\SYSTEM\CurrentControlSet\Control\Print\Monitors\&lt;<i>MonitorName</i>&gt;\Ports</b>



Call the <a href="f99774d4-575b-43a3-8887-e15acb0477fd">RegSetValueEx</a> function to set these values.

<table>
<tr>
<th>Port monitor setting</th>
<th>Data type</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>StatusUpdateEnabled</b></td>
<td><b>REG_DWORD</b></td>
<td>
If a nonzero value, enables the port monitor to update the spooler with the port status.

</td>
</tr>
<tr>
<td><b>StatusUpdateInterval</b></td>
<td><b>REG_DWORD</b></td>
<td>
Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.

</td>
</tr>
</table>
 

In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default. Client-side rendering of a print jobs can be configured for each printer by setting the following values in <i>pValueName</i>.

<table>
<tr>
<th>Setting</th>
<th>Data type</th>
<th>Description</th>
</tr>
<tr>
<td><b>EMFDespoolingSetting</b></td>
<td><b>REG_DWORD</b></td>
<td>
A value of 
0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.

A value of 1 disables client-side rendering of print jobs.

</td>
</tr>
<tr>
<td><b>ForceClientSideRendering</b></td>
<td><b>REG_DWORD</b></td>
<td>
A value of 
0, or if this value is not present in the registry,    causes the print jobs to be  rendered on the client. If a print job cannot be rendered on the client, it will be rendered on the server. If a print job cannot be rendered on the server, it will fail.

A value of 1 will render print jobs on the client. If a print job cannot be rendered on the client, it will fail.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>



<a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>
 

 

