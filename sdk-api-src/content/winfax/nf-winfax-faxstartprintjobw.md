---
UID: NF:winfax.FaxStartPrintJobW
title: FaxStartPrintJobW function
author: windows-sdk-content
description: A fax client application calls the FaxStartPrintJob function to start printing an outbound fax transmission on the specified fax printer.
old-location: fax\_mfax_faxstartprintjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3dwi.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxStartPrintJob, FaxStartPrintJob function [Fax Service], FaxStartPrintJobA, FaxStartPrintJobW, _mfax_faxstartprintjob, fax._mfax_faxstartprintjob, winfax/FaxStartPrintJob, winfax/FaxStartPrintJobA, winfax/FaxStartPrintJobW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxStartPrintJobW (Unicode) and FaxStartPrintJobA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxStartPrintJob
 - FaxStartPrintJobA
 - FaxStartPrintJobW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxStartPrintJobW function


## -description


A fax client application calls the <b>FaxStartPrintJob</b> function to start printing an outbound fax transmission on the specified fax printer.


## -parameters




### -param PrinterName [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that contains the name of a fax printer. The string can specify one of the following: 

                    


<ul>
<li>A local printer, such as, "<i>printername</i>"</li>
<li>A network printer, such as "\\<i>machinename</i>\<i>printername</i>"</li>
<li><b>NULL</b> to specify the local fax printer</li>
</ul>



### -param PrintInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/d0123f3d-4593-409e-a810-0fc4c699de81">FAX_PRINT_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d0123f3d-4593-409e-a810-0fc4c699de81">FAX_PRINT_INFO</a> structure that contains the information necessary for the fax server to print the fax transmission. The structure includes, among other items, the recipient's fax number, sender and recipient data, an optional billing code, and delivery report information. For more information, see the following Remarks section.


### -param FaxJobId [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the print spooler's unique ID for the fax print job. (This is not the same as the fax queue's ID for the job and it cannot be used as a parameter in any fax API that takes a fax ID parameter.) This parameter is required.


### -param FaxContextInfo [out]

Type: <b>PFAX_CONTEXT_INFO</b>

Pointer to a <a href="https://msdn.microsoft.com/6eef1d9e-0107-4882-884b-8ba78c4e73c4">FAX_CONTEXT_INFO</a> structure to receive a handle to a printer device context. When the fax client application calls the <a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a> function, it must pass this value in that function's <i>FaxContextInfo</i> parameter. For more information, see <a href="_win32_Device_Contexts">Device Contexts</a> and the <a href="_win32_Printing_and_Print_Spooler_Reference">Printing and Print Spooler Reference</a>.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>PrintInfo</i> or <i>FaxContextInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <b>RecipientNumber</b> member of the <a href="https://msdn.microsoft.com/d0123f3d-4593-409e-a810-0fc4c699de81">FAX_PRINT_INFO</a> structure is <b>NULL</b>; or the <b>OutputFileName</b> member is <b>NULL</b> and the <b>RecipientNumber</b> member is not specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PRINTER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>PrinterName</i> parameter specifies a printer that is not a fax printer, or there is no fax printer installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SPL_NO_STARTDOC</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/219cc7f7-d5c8-416b-b9ea-0f13584cac57">FaxStartPrintJob</a> was not called first, hence there was no <a href="_win32_StartDoc">StartDoc</a> call.

</td>
</tr>
</table>
 




## -remarks



The function returns a handle to a device context. The handle is used by the <a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a> function, and by the <a href="_win32_AbortDoc">AbortDoc</a>, <a href="_win32_EndDoc">EndDoc</a>, <a href="_win32_DeleteDC">DeleteDC</a>, <a href="_win32_StartPage">StartPage</a>, <a href="_win32_EndPage">EndPage</a> and other Win32 Windows Graphics Device Interface (GDI) functions.

<div class="alert"><b>Note</b>  The application must also call the <a href="_win32_AbortDoc">AbortDoc</a> function or the <a href="_win32_EndDoc">EndDoc</a> function to complete the print job, and call the <a href="_win32_DeleteDC">DeleteDC</a> function to deallocate the handle to the printer device context. For more information, see <a href="https://msdn.microsoft.com/d6e0afbd-6e64-487c-97fc-1e5cd5092d14">Printing a Fax to a Device Context</a>.</div>
<div> </div>
A fax client application should not call the <a href="_win32_CreateDC">CreateDC</a> GDI function to create the fax printer device context; nor should it call the <a href="_win32_StartPage">StartPage</a> printing function to start a fax print job. Instead, the application should call the <b>FaxStartPrintJob</b> function. This is because <b>FaxStartPrintJob</b> modifies information in the <a href="_win32_DEVMODE_str">DEVMODE</a> structure specific to the fax printer of interest.

The change prevents the display of the Fax Send Wizard that collects information from the user. The fax server uses the data in the <a href="https://msdn.microsoft.com/d0123f3d-4593-409e-a810-0fc4c699de81">FAX_PRINT_INFO</a> structure pointed to by the <i>PrintInfo</i> parameter to print the fax transmission. This structure contains data the Fax Send Wizard would have collected, had the wizard been displayed.

A fax client application must call the <b>FaxStartPrintJob</b> function before calling the <a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a> function to print a cover page with a fax job.




## -see-also




<a href="_win32_AbortDoc">AbortDoc</a>



<a href="_win32_DEVMODE_str">DEVMODE</a>



<a href="_win32_DeleteDC">DeleteDC</a>



<a href="_win32_EndDoc">EndDoc</a>



<a href="https://msdn.microsoft.com/6eef1d9e-0107-4882-884b-8ba78c4e73c4">FAX_CONTEXT_INFO</a>



<a href="https://msdn.microsoft.com/d0123f3d-4593-409e-a810-0fc4c699de81">FAX_PRINT_INFO</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/a48d4eb2-2b49-4379-a281-e5465de1af94">FaxPrintCoverPage</a>
 

 

