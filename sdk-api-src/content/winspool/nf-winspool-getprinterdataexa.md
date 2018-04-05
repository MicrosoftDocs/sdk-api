---
UID: NF:winspool.GetPrinterDataExA
title: GetPrinterDataExA function
author: windows-driver-content
description: The GetPrinterDataEx function retrieves configuration data for the specified printer or print server.
old-location: gdi\getprinterdataex.htm
old-project: printdocs
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetPrinterDataEx, GetPrinterDataEx function [Windows GDI], GetPrinterDataExA, GetPrinterDataExW, _win32_GetPrinterDataEx, gdi.getprinterdataex, winspool/GetPrinterDataEx, winspool/GetPrinterDataExA, winspool/GetPrinterDataExW
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
req.unicode-ansi: GetPrinterDataExW (Unicode) and GetPrinterDataExA (ANSI)
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
-	Ext-MS-Win-printer-Winspool-l1-1-1.dll
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	GetPrinterDataEx
-	GetPrinterDataExA
-	GetPrinterDataExW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrinterDataExA function


## -description


The <b>GetPrinterDataEx</b> function retrieves configuration data for the specified printer or print server. <b>GetPrinterDataEx</b> can retrieve values that  the <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a> function stored. In addition, <b>GetPrinterDataEx</b> can retrieve values that the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> function stored under a specified key.


## -parameters




### -param hPrinter [in]

A handle to the printer or print server for which the function retrieves configuration data. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>, <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>, or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pKeyName [in]

A pointer to a null-terminated string that specifies the key containing the value to be retrieved. Use the backslash ( \ ) character as a delimiter to specify a path that has one or more subkeys.

If <i>hPrinter</i> is a handle to a printer and <i>pKeyName</i> is <b>NULL</b> or an empty string, <b>GetPrinterDataEx</b> returns <b>ERROR_INVALID_PARAMETER</b>.

If <i>hPrinter</i> is a handle to a print server, <i>pKeyName</i> is ignored.


### -param pValueName [in]

A pointer to a null-terminated string that identifies the data to retrieve.

For printers, this string specifies the name of a value under the <i>pKeyName</i> key.

For print servers, this string is one of the predefined strings listed in the following Remarks section.


### -param pType [out]

A pointer to a variable that receives the type of data stored in the value. The function returns the type specified in the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> call when the data was stored. This parameter can be <b>NULL</b> if you don't need the information. <b>GetPrinterDataEx</b> passes <i>pType</i> on as the <i>lpdwType</i> parameter of a <a href="https://msdn.microsoft.com/202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a> function call.


### -param pData [out]

A pointer to a buffer that receives the configuration data.


### -param nSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.


### -param pcbNeeded [out]

A pointer to a variable that receives the size, in bytes, of the configuration data. If the buffer size specified by <i>nSize</i> is too small, the function returns <b>ERROR_MORE_DATA</b>, and <i>pcbNeeded</i> indicates the required buffer size.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error value.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>GetPrinterDataEx</b> retrieves printer-configuration data that was set by the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> and <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a> functions.

Calling <b>GetPrinterDataEx</b> with the <i>pKeyName</i> parameter set to "PrinterDriverData" is equivalent to calling the <a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a> function.

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
<td><b>SPLREG_ARCHITECTURE</b></td>
<td></td>
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
<td><b>SPLREG_DNS_MACHINE_NAME</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_DS_PRESENT</b></td>
<td>
On successful return, <i>pData</i> contains 0x0001 if the machine is on a DS domain, 0 otherwise.

</td>
</tr>
<tr>
<td><b>SPLREG_DS_PRESENT_FOR_USER</b></td>
<td>
On successful return, <i>pData</i> contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.

</td>
</tr>
<tr>
<td><b>SPLREG_EVENT_LOG</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_MAJOR_VERSION</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_MINOR_VERSION</b></td>
<td></td>
</tr>
<tr>
<td><b>SPLREG_NET_POPUP</b></td>
<td>
Not supported in Windows Server 2003 and later

</td>
</tr>
<tr>
<td><b>SPLREG_NET_POPUP_TO_COMPUTER</b></td>
<td>
On successful return, <i>pData</i> contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.

Not supported in Windows Server 2003 and later

</td>
</tr>
<tr>
<td><b>SPLREG_OS_VERSION</b></td>
<td>
Windows XP and later

</td>
</tr>
<tr>
<td><b>SPLREG_OS_VERSIONEX</b></td>
<td></td>
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
<td><b>SPLREG_REMOTE_FAX</b></td>
<td>
On successful return, <i>pData</i> contains 0x0001 if the FAX service supports remote clients, 0 otherwise.

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
 

The following values of <i>pValueName</i> indicate the pool printing behavior when an error occurs.

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



Call the <a href="202d253a-10ff-40e7-8eec-a49717443b81">RegQueryValueEx</a> function to query these values.

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
 

If <i>pKeyName</i> is one of the predefined Directory Service (DS) keys (see <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>) and <i>pValueName</i> contains a comma (','), then the portion of <i>pValueName</i> before the comma is the value name and the portion of <i>pValueName</i> to the right of the comma is the DS Property OID. A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key. <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> also adds the value name and data under the DS key.

In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default. The configuration of client-side rendering for a printer can be read  by setting <i>pKeyName</i> to "PrinterDriverData" and <i>pValueName</i> to the setting value in the following table.

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
0, or if this value is not present in the registry,   will cause the print jobs to be  rendered on the client. If a print job cannot be rendered on the client, it will be rendered on the server. If a print job cannot be rendered on the server, it will fail.

A value of 1 will render print jobs on the client. If a print job cannot be rendered on the client, it will fail.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>
 

 

