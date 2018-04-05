---
UID: NF:winspool.FindFirstPrinterChangeNotification
title: FindFirstPrinterChangeNotification function
author: windows-driver-content
description: The FindFirstPrinterChangeNotification function creates a change notification object and returns a handle to the object. You can then use this handle in a call to one of the wait functions to monitor changes to the printer or print server.
old-location: gdi\findfirstprinterchangenotification.htm
old-project: printdocs
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FindFirstPrinterChangeNotification, FindFirstPrinterChangeNotification function [Windows GDI], PRINTER_CHANGE_ALL, PRINTER_CHANGE_FORM, PRINTER_CHANGE_JOB, PRINTER_CHANGE_PORT, PRINTER_CHANGE_PRINTER, PRINTER_CHANGE_PRINTER_DRIVER, PRINTER_CHANGE_PRINT_PROCESSOR, PRINTER_CHANGE_SERVER, PRINTER_NOTIFY_CATEGORY_3D, PRINTER_NOTIFY_CATEGORY_ALL, _win32_FindFirstPrinterChangeNotification, gdi.findfirstprinterchangenotification, winspool/FindFirstPrinterChangeNotification
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
req.unicode-ansi: 
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
-	FindFirstPrinterChangeNotification
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FindFirstPrinterChangeNotification function


## -description


The <b>FindFirstPrinterChangeNotification</b> function creates a change notification object and returns a handle to the object. You can then use this handle in a call to one of the wait functions to monitor changes to the printer or print server.

The <b>FindFirstPrinterChangeNotification</b> call specifies the type of changes to be monitored. You can specify a set of conditions to monitor for changes, a set of printer information fields to monitor, or both.

A wait operation on the change notification handle succeeds when one of the specified changes occurs in the specified printer or print server. You then call the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function to retrieve information about the change, and to reset the change notification object for use in the next wait operation.


## -parameters




### -param hPrinter [in]

A handle to the printer or print server that you want to monitor. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param fdwFilter

The conditions that will cause the change notification object to enter a signaled state. A change notification occurs when one or more of the specified conditions are met. The <i>fdwFilter</i> parameter can be zero if <i>pPrinterNotifyOptions</i> is non-<b>NULL</b>.

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_FORM"></a><a id="printer_change_form"></a><dl>
<dt><b>PRINTER_CHANGE_FORM</b></dt>
</dl>
</td>
<td width="60%">
Notify of any changes to a form. You can set this general flag or one or more of the following specific flags:

<dl>
<dd>PRINTER_CHANGE_ADD_FORM</dd>
<dd>PRINTER_CHANGE_SET_FORM</dd>
<dd>PRINTER_CHANGE_DELETE_FORM</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_JOB"></a><a id="printer_change_job"></a><dl>
<dt><b>PRINTER_CHANGE_JOB</b></dt>
</dl>
</td>
<td width="60%">
Notify of any changes to a job. You can set this general flag or one or more of the following specific flags:

<dl>
<dd>PRINTER_CHANGE_ADD_JOB</dd>
<dd>PRINTER_CHANGE_SET_JOB</dd>
<dd>PRINTER_CHANGE_DELETE_JOB</dd>
<dd>PRINTER_CHANGE_WRITE_JOB</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_PORT"></a><a id="printer_change_port"></a><dl>
<dt><b>PRINTER_CHANGE_PORT</b></dt>
</dl>
</td>
<td width="60%">
Notify of any changes to a port. You can set this general flag or one or more of the following specific flags:

<dl>
<dd>PRINTER_CHANGE_ADD_PORT</dd>
<dd>PRINTER_CHANGE_CONFIGURE_PORT </dd>
<dd>PRINTER_CHANGE_DELETE_PORT</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_PRINT_PROCESSOR"></a><a id="printer_change_print_processor"></a><dl>
<dt><b>PRINTER_CHANGE_PRINT_PROCESSOR</b></dt>
</dl>
</td>
<td width="60%">
Notify of any changes to a print processor. You can set this general flag or one or more of the following specific flags: 

<dl>
<dd>PRINTER_CHANGE_ADD_PRINT_PROCESSOR </dd>
<dd>PRINTER_CHANGE_DELETE_PRINT_PROCESSOR</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_PRINTER"></a><a id="printer_change_printer"></a><dl>
<dt><b>PRINTER_CHANGE_PRINTER</b></dt>
</dl>
</td>
<td width="60%">
Notify of any changes to a printer. You can set this general flag or one or more of the following specific flags:

<dl>
<dd>PRINTER_CHANGE_ADD_PRINTER</dd>
<dd>PRINTER_CHANGE_SET_PRINTER</dd>
<dd>PRINTER_CHANGE_DELETE_PRINTER</dd>
<dd>PRINTER_CHANGE_FAILED_CONNECTION_PRINTER</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_PRINTER_DRIVER"></a><a id="printer_change_printer_driver"></a><dl>
<dt><b>PRINTER_CHANGE_PRINTER_DRIVER</b></dt>
</dl>
</td>
<td width="60%">
Notify of any changes to a printer driver. You can set this general flag or one or more of the following specific flags:

<dl>
<dd>PRINTER_CHANGE_ADD_PRINTER_DRIVER</dd>
<dd>PRINTER_CHANGE_SET_PRINTER_DRIVER</dd>
<dd>PRINTER_CHANGE_DELETE_PRINTER_DRIVER</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ALL"></a><a id="printer_change_all"></a><dl>
<dt><b>PRINTER_CHANGE_ALL</b></dt>
</dl>
</td>
<td width="60%">
Notify if any of the preceding changes occur.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_SERVER"></a><a id="printer_change_server"></a><dl>
<dt><b>PRINTER_CHANGE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Windows 7: Notify of any changes to the server.

This flag is not included in the changes monitored by setting the <b>PRINTER_CHANGE_ALL</b> value.

</td>
</tr>
</table>
 

For descriptions of the more specific flags in the preceding table, see the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function.


### -param fdwOptions

The flag that determines the category of printers for which notifications will work. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRINTER_NOTIFY_CATEGORY_ALL"></a><a id="printer_notify_category_all"></a><dl>
<dt><b>PRINTER_NOTIFY_CATEGORY_ALL</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> returns notifications for both 2D and 3D printers.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_NOTIFY_CATEGORY_3D"></a><a id="printer_notify_category_3d"></a><dl>
<dt><b>PRINTER_NOTIFY_CATEGORY_3D</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> returns notifications only for 3D printers.

</td>
</tr>
</table>
 

When this flag is set to zero (0), <b>FindFirstPrinterChangeNotification</b> will only work for 2D printers. This is the default value.


### -param pPrinterNotifyOptions [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/712c546d-dbb3-4f78-b14e-fbb8619b57f9">PRINTER_NOTIFY_OPTIONS</a> structure. The <b>pTypes</b> member of this structure is an array of one or more <a href="https://msdn.microsoft.com/1009f892-d3a8-4887-99b4-a35d1268eeb4">PRINTER_NOTIFY_OPTIONS_TYPE</a> structures, each of which specifies a printer information field to monitor. A change notification occurs when one or more of the specified fields changes. When a change occurs, the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function can retrieve the new printer information. This parameter can be <b>NULL</b> if <i>fdwFilter</i> is nonzero.

For a list of fields that can be monitored, see <a href="https://msdn.microsoft.com/1009f892-d3a8-4887-99b4-a35d1268eeb4">PRINTER_NOTIFY_OPTIONS_TYPE</a>.


## -returns



If the function succeeds, the return value is a handle to a change notification object associated with the specified printer or print server.

If the function fails, the return value is INVALID_HANDLE_VALUE. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
To monitor a printer or print server, call the <b>FindFirstPrinterChangeNotification</b> function, then use the returned change notification object handle in a call to one of the <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. A wait operation on a change notification object is satisfied when the change notification object enters the signaled state. The system signals the object when one or more of the changes specified by <i>fdwFilter</i> or <i>pPrinterNotifyOptions</i> occurs in the monitored printer or print server.

When you call <b>FindFirstPrinterChangeNotification</b>, either <i>fdwFilter</i> must be nonzero or <i>pPrinterNotifyOptions</i> must be non-<b>NULL</b>. If both are specified, notifications will occur for both.

When a wait operation on a printer change notification object is satisfied, call the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function to determine the cause of the notification. For a condition specified by <i>fdwFilter</i>, <b>FindNextPrinterChangeNotification</b> reports the condition or conditions that changed. For a printer information field specified by <i>pPrinterNotifyOptions</i>, <b>FindNextPrinterChangeNotification</b> reports the field or fields that changed as well as the new information for these fields. <b>FindNextPrinterChangeNotification</b> also resets the change notification object to the nonsignaled state so you can use it in another wait operation to continue monitoring the printer or print server.

With one exception, do not call the <a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a> function if the change notification object is not in the signaled state. If the wait function returns the value WAIT_TIMEOUT, the change object is not in the signaled state. Call the <b>FindNextPrinterChangeNotification</b> function only if the wait function succeeds without timing out. The exception is when <b>FindNextPrinterChangeNotification</b> is called with the PRINTER_NOTIFY_OPTIONS_REFRESH bit set in the <i>pPrinterNotifyOptions</i> parameter.

When you no longer need the change notification object, close it by calling the <a href="https://msdn.microsoft.com/2b4758f8-af0a-494b-8f1b-8ea6ee73c79b">FindClosePrinterChangeNotification</a> function.

Callers of <b>FindFirstPrinterChangeNotification</b> must ensure that the printer handle passed into <b>FindFirstPrinterChangeNotification</b> remains valid until <a href="https://msdn.microsoft.com/2b4758f8-af0a-494b-8f1b-8ea6ee73c79b">FindClosePrinterChangeNotification</a> is called. If the printer handle is closed before the printer change notification handle, further notifications will fail to be delivered.

<b>FindFirstPrinterChangeNotification</b> will not send change notifications for 3D printers to server handles.

<div class="alert"><b>Note</b>  
        In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled. If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server. A machine admin will have to enable exception.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2b4758f8-af0a-494b-8f1b-8ea6ee73c79b">FindClosePrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/ea7774ae-361f-41e4-bbc6-3f100028b22a">FindNextPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/712c546d-dbb3-4f78-b14e-fbb8619b57f9">PRINTER_NOTIFY_OPTIONS</a>



<a href="https://msdn.microsoft.com/1009f892-d3a8-4887-99b4-a35d1268eeb4">PRINTER_NOTIFY_OPTIONS_TYPE</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

