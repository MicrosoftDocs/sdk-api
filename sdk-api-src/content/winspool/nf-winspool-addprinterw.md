---
UID: NF:winspool.AddPrinterW
title: AddPrinterW function
author: windows-driver-content
description: The AddPrinter function adds a printer to the list of supported printers for a specified server.
old-location: gdi\addprinter.htm
old-project: printdocs
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddPrinter, AddPrinter function [Windows GDI], AddPrinterA, AddPrinterW, _win32_AddPrinter, gdi.addprinter, winspool/AddPrinter, winspool/AddPrinterA, winspool/AddPrinterW
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
req.unicode-ansi: AddPrinterW (Unicode) and AddPrinterA (ANSI)
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
api_name:
-	AddPrinter
-	AddPrinterA
-	AddPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrinterW function


## -description


The <b>AddPrinter</b> function adds a printer to the list of supported printers for a specified server.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed. If this string is <b>NULL</b>, the printer is installed locally.


### -param Level [in]

The version of the structure to which <i>pPrinter</i> points. This value must be 2.


### -param pPrinter [in]

A pointer to a <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure that contains information about the printer. You must specify non-<b>NULL</b> values for the <b>pPrinterName</b>, <b>pPortName</b>, <b>pDriverName</b>, and <b>pPrintProcessor</b> members of this structure before calling <b>AddPrinter</b>.


## -returns



If the function succeeds, the return value is a handle (not thread safe) to a new printer object. When you are finished with the handle, pass it to the <a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a> function to close it.

If the function fails, the return value is <b>NULL</b>. 




## -remarks



Do not call this method in <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>.

<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.

The returned handle is not thread safe. If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the <a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>. To avoid writing custom code the application can open a printer handle on each thread, as needed.

The following are the members of the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure that can be set before the <b>AddPrinter</b> function is called:

<ul>
<li><b>Attributes</b></li>
<li><b>pPrintProcessor</b></li>
<li><b>DefaultPriority</b></li>
<li><b>Priority</b></li>
<li><b>pComment</b></li>
<li><b>pSecurityDescriptor</b></li>
<li><b>pDatatype</b></li>
<li><b>pSepFile</b></li>
<li><b>pDevMode</b></li>
<li><b>pShareName</b></li>
<li><b>pLocation</b></li>
<li><b>StartTime</b></li>
<li><b>pParameters</b></li>
<li><b>UntilTime</b></li>
</ul>
The <b>Status</b>, <b>cJobs</b>, and <b>AveragePPM</b> members of the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure are reserved for use by the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function. They must not be set before calling <b>AddPrinter</b>.


         If <b>pSecurityDescriptor</b> is <b>NULL</b>, the system assigns a default security descriptor to the printer. The default security descriptor has the following permissions.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>Administrators and Power Users</td>
<td>Full control on the print queue. This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.

</td>
</tr>
<tr>
<td>Creator/Owner</td>
<td>Can manage own jobs. This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</td>
</tr>
<tr>
<td>Everyone</td>
<td>Execute and standard read control. This means that members of the everyone group can print and read properties of the print queue.</td>
</tr>
</table>
 

After an application creates a printer object with the <b>AddPrinter</b> function, it must use the <a href="https://msdn.microsoft.com/1d4c961b-178b-47af-b983-5b7327919f93">PrinterProperties</a> function to specify the correct settings for the printer driver associated with the printer object.

The <b>AddPrinter</b> function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion. In that case, the existing printer is not deleted, and the <b>AddPrinter</b> creation parameters are used to change the existing printer settings (as if the application had used the <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> function).

Use the <a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a> function to enumerate the set of print processors installed on a server. Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548757">EnumPrintProcessorDatatypes</a> function to enumerate the set of data types that a print processor supports. Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a> function to enumerate the set of available ports. Use the <a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a> function to enumerate the installed printer drivers.


         The caller of the <b>AddPrinter</b> function must have SERVER_ACCESS_ADMINISTER access to the server on which the printer is to be created. The handle returned by the function will have PRINTER_ALL_ACCESS permission, and can be used to perform administrative operations on the printer.


         If the <b>DrvPrinterEvent</b> function is passed the PRINTER_EVENT_FLAG_NO_UI flag, the driver should not use a UI call during <b>DrvPrinterEvent</b>. To do UI-related jobs, the installer should either use the <b>VendorSetup</b> entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer. For more information about <b>VendorSetup</b>, see the Microsoft Windows Driver Development Kit (DDK).


         The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run <b>AddPrinter</b>.




## -see-also




<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548757">EnumPrintProcessorDatatypes</a>



<a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/1d4c961b-178b-47af-b983-5b7327919f93">PrinterProperties</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

