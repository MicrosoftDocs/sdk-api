---
UID: NF:winspool.OpenPrinterW
title: OpenPrinterW function
author: windows-driver-content
description: The OpenPrinter function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.
old-location: gdi\openprinter.htm
old-project: printdocs
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: OpenPrinter, OpenPrinter function [Windows GDI], OpenPrinterA, OpenPrinterW, _win32_OpenPrinter, gdi.openprinter, winspool/OpenPrinter, winspool/OpenPrinterA, winspool/OpenPrinterW
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
req.unicode-ansi: OpenPrinterW (Unicode) and OpenPrinterA (ANSI)
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
-	Ext-MS-Win-printer-Winspool-l1-1-0.dll
-	Ext-MS-Win-printer-Winspool-l1-1-1.dll
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	OpenPrinter
-	OpenPrinterA
-	OpenPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenPrinterW function


## -description


The <b>OpenPrinter</b> function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.


## -parameters




### -param pPrinterName [in]

A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.

For a printer object use: PrinterName, Job xxxx. For an XcvMonitor, use: ServerName, XcvMonitor MonitorName. For an XcvPort, use: ServerName, XcvPort PortName.

If <b>NULL</b>, it indicates the local printer server.


### -param phPrinter [out]

A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.

The <i>phPrinter</i> parameter can return an Xcv handle for use with the XcvData function. For more information about XcvData, see the DDK.


### -param pDefault [in]

A pointer to a <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure. This value can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.




## -remarks



Do not call this method in <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>.

<div class="alert"><b>Note</b>  A handle obtained for a remote printer by a call to <b>OpenPrinter</b> for a remote printer accesses the printer through a local cache in the print spooler service.
This cache isn't real-time accurate.
To obtain accurate data, replace the OpenPrinter call with <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> with pOptions.dwFlags set to PRINTER_OPTION_NO_CACHE.  Note that only OpenPrinter2W is functional.
The function returns a printer handle that uses other Printing API calls and bypasses the local cache. 
This method blocks while waiting for network communication with the remote printer, so it might not return immediately.
How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application.  Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</div>
<div> </div>
<div class="alert"><b>Note</b>  A handle obtained by a call to <b>OpenPrinter</b> for a remote printer will access the printer through a local cache in the print spooler service.
This cache is, by design, not real time accurate.
If you need to obtain accurate data, replace the <b>OpenPrinter</b> call with <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> with <i>pOptions.dwFlags</i> set to <a href="https://msdn.microsoft.com/7cc3d10c-8bc2-4899-b083-63d802ee16e7">PRINTER_OPTION_NO_CACHE</a>. Note that only <b>OpenPrinter2W</b> is functional.
Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache. 
Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.
How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application. Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The handle pointed to by <i>phPrinter</i> is not thread safe. If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the <a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>. To avoid writing custom code the application can open a printer handle on each thread, as needed.

The <i>pDefault</i> parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a> function. However, you can override these values by using the <a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a> function after a document has been started.

The <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> settings defined in the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure of the <i>pDefault</i> parameter are not used when the value of the <i>pDatatype</i> member of the <a href="https://msdn.microsoft.com/142d988b-dd74-4312-8b27-331a7ec70344">DOC_INFO_1</a> structure that was passed in the  <i>pDocInfo</i> parameter of the <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a> call is "RAW". When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with <i>pDatatype</i> set to "RAW", the document must fully describe the <b>DEVMODE</b>-style print job settings in the language understood by the hardware.

You can call the <b>OpenPrinter</b> function to open a handle to a print server or to determine the access rights that a client has to a print server. To do so, specify the name of the print server in the <i>pPrinterName</i> parameter, set the <b>pDatatype</b> and <b>pDevMode</b> members of the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure to <b>NULL</b>, and set the <b>DesiredAccess</b> member to specify a server access mask value such as SERVER_ALL_ACCESS. When you finish with the handle, pass it to the <a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a> function to close it.

Use the <b>DesiredAccess</b> member of the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure to specify the access rights that you need to the printer. The access rights can be one of the following. (If <i>pDefault</i> is <b>NULL</b>, then the access rights are PRINTER_ACCESS_USE.)

<table>
<tr>
<th>Desired Access value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ACCESS_ADMINISTER</td>
<td>To perform administrative tasks, such as those provided by <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>.</td>
</tr>
<tr>
<td>PRINTER_ACCESS_USE</td>
<td>To perform basic printing operations.</td>
</tr>
<tr>
<td>PRINTER_ALL_ACCESS</td>
<td>To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.</td>
</tr>
<tr>
<td>PRINTER_ACCESS_MANAGE_LIMITED</td>
<td>To perform administrative tasks, such as those provided by <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> and <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a>. This value is available starting from Windows 8.1.</td>
</tr>
<tr>
<td>generic security values, such as WRITE_DAC</td>
<td>To allow specific control access rights. See <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.</td>
</tr>
</table>
 

If a user does not have permission to open a specified printer or print server with the desired access, the <b>OpenPrinter</b> call will fail with a return value of zero and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return the value ERROR_ACCESS_DENIED.


#### Examples

For a sample program that uses this function, see <a href="https://msdn.microsoft.com/C212DD92-2B90-45BC-8746-29C193FBDF69">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>



<a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>
 

 

