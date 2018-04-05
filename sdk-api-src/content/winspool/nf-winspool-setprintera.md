---
UID: NF:winspool.SetPrinterA
title: SetPrinterA function
author: windows-driver-content
description: The SetPrinter function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.
old-location: gdi\setprinter.htm
old-project: printdocs
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 0, 2, 3, 4, 5, 6, 7, 8, 9, PRINTER_CONTROL_PAUSE, PRINTER_CONTROL_PURGE, PRINTER_CONTROL_RESUME, PRINTER_CONTROL_SET_STATUS, SetPrinter, SetPrinter function [Windows GDI], SetPrinterA, SetPrinterW, _win32_SetPrinter, gdi.setprinter, winspool/SetPrinter, winspool/SetPrinterA, winspool/SetPrinterW
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
req.unicode-ansi: SetPrinterW (Unicode) and SetPrinterA (ANSI)
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
-	WinSpool.drv
-	Ext-MS-Win-printer-WinSpool-l1-1-0.dll
-	Ext-MS-Win-printer-WinSpool-l1-1-1.dll
-	Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	SetPrinter
-	SetPrinterA
-	SetPrinterW
product: Windows
targetos: Windows
req.lib: WinSpool.lib
req.dll: WinSpool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetPrinterA function


## -description


The <b>SetPrinter</b> function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.


## -parameters




### -param hPrinter [in]

A handle to the printer. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>, <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>, or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param Level [in]

The type of data that the function stores into the buffer pointed to by <i>pPrinter</i>. If the <i>Command</i> parameter is not equal to zero, the <i>Level</i> parameter must be zero.

This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.


### -param pPrinter [in]

A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the <i>Command</i> parameter. The type of data in the buffer is determined by the value of <i>Level</i>.

<table>
<tr>
<th>Level</th>
<th>Structure</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
If the <i>Command</i> parameter is <b>PRINTER_CONTROL_SET_STATUS</b>, <i>pPrinter</i> must contain a <b>DWORD</b> value that specifies the new printer status to set. For a list of the possible status values, see the <b>Status</b> member of the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure. Note that <b>PRINTER_STATUS_PAUSED</b> and <b>PRINTER_STATUS_PENDING_DELETION</b> are not valid status values to set.

If <i>Level</i> is 0, but the <i>Command</i> parameter is not <b>PRINTER_CONTROL_SET_STATUS</b>, <i>pPrinter</i> must be <b>NULL</b>.

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
A <a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a> structure. The <i>dwAction</i> member of this structure indicates whether <b>SetPrinter</b> should publish, unpublish, re-publish, or update the printer's data in the directory service.

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
 


### -param Command [in]

The action to perform.

If the <i>Level</i> parameter is nonzero, set the value of this parameter to  zero. In this case, the printer retains its current state and the function reconfigures the printer data as specified by the <i>Level</i> and <i>pPrinter</i> parameters.

If the <i>Level</i> parameter is zero, set the value of this parameter to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CONTROL_PAUSE"></a><a id="printer_control_pause"></a><dl>
<dt><b>PRINTER_CONTROL_PAUSE</b></dt>
</dl>
</td>
<td width="60%">
Pause the printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CONTROL_PURGE"></a><a id="printer_control_purge"></a><dl>
<dt><b>PRINTER_CONTROL_PURGE</b></dt>
</dl>
</td>
<td width="60%">
Delete all print jobs in the printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CONTROL_RESUME"></a><a id="printer_control_resume"></a><dl>
<dt><b>PRINTER_CONTROL_RESUME</b></dt>
</dl>
</td>
<td width="60%">
Resume a paused printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CONTROL_SET_STATUS"></a><a id="printer_control_set_status"></a><dl>
<dt><b>PRINTER_CONTROL_SET_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Set the printer status.

Set the <i>pPrinter</i> parameter to a pointer to a <b>DWORD</b> value that specifies the new printer status.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.

If <i>Level</i> is 7 and the publish action failed, <b>SetPrinter</b> returns <b>ERROR_IO_PENDING</b> and attempts to complete the action in the background. If <i>Level</i> is 7 and the update action failed, <b>SetPrinter</b> returns <b>ERROR_FILE_NOT_FOUND</b>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
You cannot use <b>SetPrinter</b> to change the default printer.

To modify the current printer settings, call the <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a> function to retrieve the current settings into a <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure, modify the members of that structure as necessary, and then call <b>SetPrinter</b>.

The <b>SetPrinter</b> function ignores the <b>pServerName</b>, <b>AveragePPM</b>, <b>Status</b>, and <b>cJobs</b> members of a <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure.

Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing. Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed. If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.

If you use <b>SetPrinter</b> to modify the default <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure for a printer (globally setting the printer defaults), you must first call the <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a> function to validate the <b>DEVMODE</b> structure.

For the <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> and <a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a> structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify. To set particular security descriptor components, you must specify the necessary access rights when you call the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> function to retrieve a handle to the printer. The following table shows the access rights required to modify the various security descriptor components.

<table>
<tr>
<th>Access permission</th>
<th>Security descriptor component</th>
</tr>
<tr>
<td><b>WRITE_OWNER</b></td>
<td>
Owner

Primary group

</td>
</tr>
<tr>
<td><b>WRITE_DAC</b></td>
<td>Discretionary access-control list (DACL)</td>
</tr>
<tr>
<td><b>ACCESS_SYSTEM_SECURITY</b></td>
<td>System access-control list (SACL)</td>
</tr>
</table>
 

If the security descriptor contains a component that the caller does not have the access right to modify, <b>SetPrinter</b> fails. Those components of a security descriptor that you don't want to modify should be <b>NULL</b> or not be present, as appropriate. If you do not want to modify the security descriptor, and are calling <b>SetPrinter</b> with a <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a> structure, set the <b>pSecurityDescriptor</b> member of that structure to <b>NULL</b>.

The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled. If <b>SetPrinter</b> is called by a machine admin, it enables the exception. If it is called by a non-admin and the exception has not already been enabled, the call fails.

You can use level 7 with the <a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a> structure to publish, unpublish, or update directory service data for the printer. The directory service data for a printer includes all the data stored under the SPLDS_* keys by calls to the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> function for the printer. Before calling <b>SetPrinter</b>, set the <b>pszObjectGUID</b> member of <b>PRINTER_INFO_7</b> to <b>NULL</b> and set the <i>dwAction</i> member to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>DSPRINT_PUBLISH</b>

</td>
<td>
Publishes the directory service data.

</td>
</tr>
<tr>
<td>
<b>DSPRINT_REPUBLISH</b>

</td>
<td>
The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer. Re-publishing also changes the GUID of the published printer. Use this value if you suspect the printer's published data has been corrupted.

</td>
</tr>
<tr>
<td>
<b>DSPRINT_UNPUBLISH</b>

</td>
<td>
Unpublishes the directory service data.

</td>
</tr>
<tr>
<td>
<b>DSPRINT_UPDATE</b>

</td>
<td>
Updates the directory service data. This is the same as <b>DSPRINT_PUBLISH</b>, except that <b>SetPrinter</b> fails with <b>ERROR_FILE_NOT_FOUND</b> if the printer is not already published.

Use <b>DSPRINT_UPDATE</b> to update published properties but not force publishing. Printer drivers should always use <b>DSPRINT_UPDATE</b> rather than <b>DSPRINT_PUBLISH</b>.

</td>
</tr>
</table>
 

<b>DSPRINT_PENDING </b>is not a valid <i>dwAction</i> value for <b>SetPrinter</b>.




## -see-also




<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/c8599f2e-3b7c-4fde-a340-ca7d3ddaa106">PRINTER_INFO_5</a>



<a href="https://msdn.microsoft.com/f26fe75b-7c97-47ad-892f-d9e40331fa5d">PRINTER_INFO_6</a>



<a href="https://msdn.microsoft.com/9443855e-df7d-41a1-a0df-5649a97b2915">PRINTER_INFO_7</a>



<a href="https://msdn.microsoft.com/98f26a45-5302-4358-bed6-691d9bc37554">PRINTER_INFO_8</a>



<a href="https://msdn.microsoft.com/8bafb995-f31c-46e3-a950-45e240c678aa">PRINTER_INFO_9</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>
 

 

