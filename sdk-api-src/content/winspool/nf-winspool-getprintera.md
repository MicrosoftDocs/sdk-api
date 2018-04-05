---
UID: NF:winspool.GetPrinterA
title: GetPrinterA function
author: windows-driver-content
description: The GetPrinter function retrieves information about a specified printer.
old-location: gdi\getprinter.htm
old-project: printdocs
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 1, 2, 3, 4, 5, 6, 7, 8, 9, GetPrinter, GetPrinter function [Windows GDI], GetPrinterA, GetPrinterW, _win32_GetPrinter, gdi.getprinter, winspool/GetPrinter, winspool/GetPrinterA, winspool/GetPrinterW
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
req.unicode-ansi: GetPrinterW (Unicode) and GetPrinterA (ANSI)
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
-	GetPrinter
-	GetPrinterA
-	GetPrinterW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrinterA function


## -description


The <b>GetPrinter</b> function retrieves information about a specified printer.


## -parameters




### -param hPrinter [in]

A handle to the printer for which the function retrieves information. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param Level [in]

The level or type of structure that the function stores into the buffer pointed to by <i>pPrinter</i>.

This value can be 1, 2, 3, 4, 5, 6, 7, 8 or 9.


### -param pPrinter [out]

A pointer to a buffer that receives a structure containing information about the specified printer. The buffer must be large enough to receive the structure and any strings or other data to which the structure members point. If the buffer is too small, the <i>pcbNeeded</i> parameter returns the required buffer size.

The type of structure is determined by the value of  <i>Level</i>.

<table>
<tr>
<th>Level</th>
<th>Structure</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a> structure containing general printer information.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure containing detailed information about the printer.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a> structure containing the printer's security information.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a> structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a> structure containing printer information such as printer attributes and time-out settings.

</td>
</tr>
<tr>
<td width="40%"><a id="6"></a><dl>
<dt><b>6</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/f26fe75b-7c97-47ad-892f-d9e40331fa5d">PRINTER_INFO_6</a> structure specifying the status value of a printer.

</td>
</tr>
<tr>
<td width="40%"><a id="7"></a><dl>
<dt><b>7</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a> structure that indicates whether the printer is published in the directory service.

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/98f26a45-5302-4358-bed6-691d9bc37554">PRINTER_INFO_8</a> structure specifying the global default printer settings.

</td>
</tr>
<tr>
<td width="40%"><a id="9"></a><dl>
<dt><b>9</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/8bafb995-f31c-46e3-a950-45e240c678aa">PRINTER_INFO_9</a> structure specifying the per-user default printer settings.

</td>
</tr>
</table>
 


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pPrinter</i>.


### -param pcbNeeded [out]

A pointer to a variable that the function sets to the size, in bytes, of the printer information. If <i>cbBuf</i> is smaller than this value, <b>GetPrinter</b> fails, and the value represents the required buffer size. If <i>cbBuf</i> is equal to or greater than this value, <b>GetPrinter</b> succeeds, and the value represents the number of bytes stored in the buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <b>pDevMode</b> member in the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>, <a href="https://msdn.microsoft.com/98f26a45-5302-4358-bed6-691d9bc37554">PRINTER_INFO_8</a>, and <a href="https://msdn.microsoft.com/8bafb995-f31c-46e3-a950-45e240c678aa">PRINTER_INFO_9</a> structures can be <b>NULL</b>. When this happens, the printer is unusable until the driver is reinstalled successfully.

For the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> and <a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a> structures that contain a pointer to a security descriptor, the function retrieves only those components of the security descriptor that the caller has permission to read. To retrieve particular security descriptor components, you must specify the necessary access rights when you call the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> function to retrieve a handle to the printer. The following table shows the access rights required to read the various security descriptor components.

<table>
<tr>
<th>Access Right</th>
<th>Security Descriptor Component</th>
</tr>
<tr>
<td>
READ_CONTROL

</td>
<td>
Owner

Primary group

Discretionary access-control list (DACL)

</td>
</tr>
<tr>
<td>
ACCESS_SYSTEM_SECURITY

</td>
<td>
System access-control list (SACL)

</td>
</tr>
</table>
 

If you specify level 7, the <b>dwAction</b> member of <a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a> returns one of the following values to indicate whether the printer is published in the directory service.

<table>
<tr>
<th>dwAction value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DSPRINT_PUBLISH</td>
<td>The printer is published. The <b>pszObjectGUID</b> member contains the GUID of the directory services print queue object associated with the printer.</td>
</tr>
<tr>
<td>DSPRINT_UNPUBLISH</td>
<td>The printer is not published.</td>
</tr>
<tr>
<td>DSPRINT_PENDING</td>
<td>Indicates that the system is attempting to complete a publish or unpublish operation. If a <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> call fails to publish or unpublish a printer, the system makes further attempts to complete the operation in the background.</td>
</tr>
</table>
 

Starting with
          Windows Vista, the printer data returned by <b>GetPrinter</b> is retrieved from a local cache when <i>hPrinter</i> refers to a printer hosted by a print server and there is at least one open connection to the print server. In all other configurations, the printer data is queried from the print server.




## -see-also




<a href="https://msdn.microsoft.com/b361fba5-e4e7-4c9e-ab32-b8ab88dcb1dc">AbortPrinter</a>



<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/04d9c073-b795-4307-ba89-d4984bc5b354">DeletePrinter</a>



<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a>



<a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a>



<a href="https://msdn.microsoft.com/98f26a45-5302-4358-bed6-691d9bc37554">PRINTER_INFO_8</a>



<a href="https://msdn.microsoft.com/8bafb995-f31c-46e3-a950-45e240c678aa">PRINTER_INFO_9</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

