---
UID: NF:winspool.OpenPrinter2A
title: OpenPrinter2A function
author: windows-driver-content
description: Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.
old-location: gdi\openprinter2.htm
old-project: printdocs
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: OpenPrinter2, OpenPrinter2 function [Windows GDI], OpenPrinter2A, OpenPrinter2W, _win32_OpenPrinter2, gdi.openprinter2, winspool/OpenPrinter2, winspool/OpenPrinter2A, winspool/OpenPrinter2W
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenPrinter2W (Unicode) and OpenPrinter2A (ANSI)
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
-	Spoolss.dll
api_name:
-	OpenPrinter2
-	OpenPrinter2A
-	OpenPrinter2W
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenPrinter2A function


## -description


Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.


## -parameters




### -param pPrinterName [in]

A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.

For a printer object, use: PrinterName,Job xxxx. For an XcvMonitor, use: ServerName,XcvMonitor MonitorName. For an XcvPort, use: ServerName,XcvPort PortName.

<b>Windows Vista:</b> If <b>NULL</b>, it indicates the local print server.


### -param phPrinter [out]

A pointer to a variable that receives a handle to the open printer or print server object.


### -param pDefault [in]

A pointer to a <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure. This value can be <b>NULL</b>.


### -param pOptions [in]

A pointer to a <a href="https://msdn.microsoft.com/7cc3d10c-8bc2-4899-b083-63d802ee16e7">PRINTER_OPTIONS</a> structure. This value can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not call this method in <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>.

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The ANSI version of this function is not implemented and returns ERROR_NOT_SUPPORTED.

The <i>pDefault</i> parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a> function. However, you can override these values by using the <a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a> function after a document has been started.

You can call the <b>OpenPrinter2</b> function to open a handle to a print server or to determine client access rights to a print server. To do this, specify the name of the print server in the <i>pPrinterName</i> parameter, set the <b>pDatatype</b> and <b>pDevMode</b> members of the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure to <b>NULL</b>, and set the <b>DesiredAccess</b> member to specify a server access mask value such as SERVER_ALL_ACCESS. When you are finished with the handle, pass it to the <a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a> function to close it.

Use the <b>DesiredAccess</b> member of the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure to specify the necessary access rights. The access rights can be one of the following.

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
<td>To perform all administrative tasks and basic printing operations except SYNCHRONIZE. See <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.</td>
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
 

If a user does not have permission to open a specified printer or print server with the desired access, the <b>OpenPrinter2</b> call will fail, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return the value ERROR_ACCESS_DENIED.

When <i>pPrinterName</i> is a local printer, then <b>OpenPrinter2</b> ignores all values of the <b>dwFlags</b> that the <a href="https://msdn.microsoft.com/7cc3d10c-8bc2-4899-b083-63d802ee16e7">PRINTER_OPTIONS</a> structure pointed to using <i>pOptions</i>, except PRINTER_OPTION_CLIENT_CHANGE. If the latter is passed, then <b>OpenPrinter2</b> will return ERROR_ACCESS_DENIED. Accordingly, when opening a local printer, <b>OpenPrinter2</b> provides no advantage over <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>.

<b>Windows Vista:</b> The printer data returned by <b>OpenPrinter2</b> is retrieved from a local cache unless the <b>PRINTER_OPTION_NO_CACHE</b> flag is set in the <b>dwFlags</b> field of the <a href="https://msdn.microsoft.com/7cc3d10c-8bc2-4899-b083-63d802ee16e7">PRINTER_OPTIONS</a> structure referenced by <i>pOptions</i>.


#### Examples

In this example, <b>OpenPrinter2</b> fails when PRINTER_ACCESS_MANAGE_LIMITED is passed to the <a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a> structure, and the user does not have the appropriate permission.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L”QueueWithNoAdminRights”, // Queue name
                     &amp;printer,                  // Printer handle
                     &amp;defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
</pre>
</td>
</tr>
</table></span></div>
For a sample program that shows how to use this function, see <a href="https://msdn.microsoft.com/C212DD92-2B90-45BC-8746-29C193FBDF69">How To: Print Using the GDI Print API</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/df29c3a6-b1d1-4d40-887d-5ffc032a5871">PRINTER_DEFAULTS</a>



<a href="https://msdn.microsoft.com/7cc3d10c-8bc2-4899-b083-63d802ee16e7">PRINTER_OPTIONS</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>
 

 

