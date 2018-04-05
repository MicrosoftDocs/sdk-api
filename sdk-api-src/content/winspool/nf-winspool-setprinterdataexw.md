---
UID: NF:winspool.SetPrinterDataExW
title: SetPrinterDataExW function
author: windows-driver-content
description: The SetPrinterDataEx function sets the configuration data for a printer or print server. The function stores the configuration data under the printer's registry key.
old-location: gdi\setprinterdataex.htm
old-project: printdocs
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SPLDS_DRIVER_KEY, SPLDS_SPOOLER_KEY, SPLDS_USER_KEY, SetPrinterDataEx, SetPrinterDataEx function [Windows GDI], SetPrinterDataExA, SetPrinterDataExW, _win32_SetPrinterDataEx, gdi.setprinterdataex, winspool/SetPrinterDataEx, winspool/SetPrinterDataExA, winspool/SetPrinterDataExW
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
req.unicode-ansi: SetPrinterDataExW (Unicode) and SetPrinterDataExA (ANSI)
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
-	SetPrinterDataEx
-	SetPrinterDataExA
-	SetPrinterDataExW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetPrinterDataExW function


## -description


The <b>SetPrinterDataEx</b> function sets the configuration data for a printer or print server. The function stores the configuration data under the printer's registry key.


## -parameters




### -param hPrinter [in]

A handle to the printer or print server for which the function sets configuration data. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>, <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>, or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pKeyName [in]

A pointer to a null-terminated string that specifies the key containing the value to set. If the specified key or subkeys do not exist, the function creates them.

To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPLDS_DRIVER_KEY"></a><a id="splds_driver_key"></a><dl>
<dt><b>SPLDS_DRIVER_KEY</b></dt>
</dl>
</td>
<td width="60%">
Printer drivers use this key to store driver properties.

</td>
</tr>
<tr>
<td width="40%"><a id="SPLDS_SPOOLER_KEY"></a><a id="splds_spooler_key"></a><dl>
<dt><b>SPLDS_SPOOLER_KEY</b></dt>
</dl>
</td>
<td width="60%">
Reserved. Used only by the print spooler to store internal spooler properties.

</td>
</tr>
<tr>
<td width="40%"><a id="SPLDS_USER_KEY"></a><a id="splds_user_key"></a><dl>
<dt><b>SPLDS_USER_KEY</b></dt>
</dl>
</td>
<td width="60%">
Applications use this key to store printer properties such as printer asset numbers.

</td>
</tr>
</table>
 

Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema. A domain administrator must create the property if it doesn't already exist. To publish a user-defined property after you use <b>SetPrinterDataEx</b> to add or change a value, call <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> with <i>Level</i> = 7 and with the <b>dwAction</b> member of <a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a> set to <b>DSPRINT_UPDATE</b>.

You can specify other keys to store non-DS configuration data. Use the backslash ( \ ) character as a delimiter to specify a path that has one or more subkeys.

If <i>hPrinter</i> is a handle to a printer and <i>pKeyName</i> is <b>NULL</b> or an empty string, <b>SetPrinterDataEx</b> returns <b>ERROR_INVALID_PARAMETER</b>.

If <i>hPrinter</i> is a handle to a print server, <i>pKeyName</i> is ignored.

Do not use <b>SPLDS_SPOOLER_KEY</b>. To change the spooler printer properties, use <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> with <i>Level</i> = 2.


### -param pValueName [in]

A pointer to a null-terminated string that identifies the data to set.

For printers, this string specifies the name of a value under the <i>pKeyName</i> key.

For print servers, this string is one of the predefined strings listed in the following Remarks section.


### -param Type [in]

A code indicating the type of data pointed to by the <i>pData</i> parameter. For a list of the possible type codes, see <a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>.

If <i>pKeyName</i> specifies one of the predefined directory service keys, <i>Type</i> must be <b>REG_SZ</b>, <b>REG_MULTI_SZ</b>, <b>REG_DWORD</b>, or <b>REG_BINARY</b>. If <b>REG_BINARY</b> is used, <i>cbData</i> must be equal to 1, and the directory service treats the data as a Boolean value.


### -param pData [in]

A pointer to a buffer that contains the printer configuration data.


### -param cbData [in]

The size, in bytes, of the array.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error value.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
To retrieve existing configuration data for a printer or print spooler, call the <a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a> function.

Calling <b>SetPrinterDataEx</b> with the <i>pKeyName</i> parameter set to "PrinterDriverData" is equivalent to calling the <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a> function.

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
 

Passing one of the following predefined values as <i>pValueName</i> sets the pool printing behavior when an error occurs.

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
 

To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled." The port monitor that supports SNMP is Standard TCP/IP port monitor.

In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default. Client-side rendering of print jobs can be configured by setting <i>pKeyName</i> to "PrinterDriverData" and <i>pValueName</i> to the setting value in the following table.

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




<a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

