---
UID: NF:winspool.FindNextPrinterChangeNotification
title: FindNextPrinterChangeNotification function
author: windows-driver-content
description: The FindNextPrinterChangeNotification function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.
old-location: gdi\findnextprinterchangenotification.htm
old-project: printdocs
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FindNextPrinterChangeNotification, FindNextPrinterChangeNotification function [Windows GDI], PRINTER_CHANGE_ADD_FORM, PRINTER_CHANGE_ADD_JOB, PRINTER_CHANGE_ADD_PORT, PRINTER_CHANGE_ADD_PRINTER, PRINTER_CHANGE_ADD_PRINTER_DRIVER, PRINTER_CHANGE_ADD_PRINT_PROCESSOR, PRINTER_CHANGE_CONFIGURE_PORT, PRINTER_CHANGE_DELETE_FORM, PRINTER_CHANGE_DELETE_JOB, PRINTER_CHANGE_DELETE_PORT, PRINTER_CHANGE_DELETE_PRINTER, PRINTER_CHANGE_DELETE_PRINTER_DRIVER, PRINTER_CHANGE_DELETE_PRINT_PROCESSOR, PRINTER_CHANGE_FAILED_CONNECTION_PRINTER, PRINTER_CHANGE_SERVER, PRINTER_CHANGE_SET_FORM, PRINTER_CHANGE_SET_JOB, PRINTER_CHANGE_SET_PRINTER, PRINTER_CHANGE_SET_PRINTER_DRIVER, PRINTER_CHANGE_TIMEOUT, PRINTER_CHANGE_WRITE_JOB, _win32_FindNextPrinterChangeNotification, gdi.findnextprinterchangenotification, winspool/FindNextPrinterChangeNotification
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
-	FindNextPrinterChangeNotification
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FindNextPrinterChangeNotification function


## -description


The <b>FindNextPrinterChangeNotification</b> function retrieves information about the most recent change notification for a change notification object associated with a printer or print server. Call this function when a wait operation on the change notification object is satisfied.

The function also resets the change notification object to the not-signaled state. You can then use the object in another wait operation to continue monitoring the printer or print server. The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function creates the change notification object and specifies the set of changes to be monitored.


## -parameters




### -param hChange [in]

A handle to a change notification object associated with a printer or print server. You obtain such a handle by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function. The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.


### -param pdwChange [out, optional]

A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification. The bit flags that might be set correspond to those specified in the <i>fdwFilter</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> call. The system sets one or more of the following bit flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ADD_FORM"></a><a id="printer_change_add_form"></a><dl>
<dt><b>PRINTER_CHANGE_ADD_FORM</b></dt>
</dl>
</td>
<td width="60%">
A form was added to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ADD_JOB"></a><a id="printer_change_add_job"></a><dl>
<dt><b>PRINTER_CHANGE_ADD_JOB</b></dt>
</dl>
</td>
<td width="60%">
A print job was sent to the printer.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ADD_PORT"></a><a id="printer_change_add_port"></a><dl>
<dt><b>PRINTER_CHANGE_ADD_PORT</b></dt>
</dl>
</td>
<td width="60%">
A port or monitor was added to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></a><a id="printer_change_add_print_processor"></a><dl>
<dt><b>PRINTER_CHANGE_ADD_PRINT_PROCESSOR</b></dt>
</dl>
</td>
<td width="60%">
A print processor was added to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ADD_PRINTER"></a><a id="printer_change_add_printer"></a><dl>
<dt><b>PRINTER_CHANGE_ADD_PRINTER</b></dt>
</dl>
</td>
<td width="60%">
A printer was added to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></a><a id="printer_change_add_printer_driver"></a><dl>
<dt><b>PRINTER_CHANGE_ADD_PRINTER_DRIVER</b></dt>
</dl>
</td>
<td width="60%">
A printer driver was added to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_CONFIGURE_PORT"></a><a id="printer_change_configure_port"></a><dl>
<dt><b>PRINTER_CHANGE_CONFIGURE_PORT</b></dt>
</dl>
</td>
<td width="60%">
A port was configured on the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_DELETE_FORM"></a><a id="printer_change_delete_form"></a><dl>
<dt><b>PRINTER_CHANGE_DELETE_FORM</b></dt>
</dl>
</td>
<td width="60%">
A form was deleted from the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_DELETE_JOB"></a><a id="printer_change_delete_job"></a><dl>
<dt><b>PRINTER_CHANGE_DELETE_JOB</b></dt>
</dl>
</td>
<td width="60%">
A job was deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_DELETE_PORT"></a><a id="printer_change_delete_port"></a><dl>
<dt><b>PRINTER_CHANGE_DELETE_PORT</b></dt>
</dl>
</td>
<td width="60%">
A port or monitor was deleted from the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></a><a id="printer_change_delete_print_processor"></a><dl>
<dt><b>PRINTER_CHANGE_DELETE_PRINT_PROCESSOR</b></dt>
</dl>
</td>
<td width="60%">
A print processor was deleted from the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_DELETE_PRINTER"></a><a id="printer_change_delete_printer"></a><dl>
<dt><b>PRINTER_CHANGE_DELETE_PRINTER</b></dt>
</dl>
</td>
<td width="60%">
A printer was deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></a><a id="printer_change_delete_printer_driver"></a><dl>
<dt><b>PRINTER_CHANGE_DELETE_PRINTER_DRIVER</b></dt>
</dl>
</td>
<td width="60%">
A printer driver was deleted from the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></a><a id="printer_change_failed_connection_printer"></a><dl>
<dt><b>PRINTER_CHANGE_FAILED_CONNECTION_PRINTER</b></dt>
</dl>
</td>
<td width="60%">
A printer connection has failed.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_SET_FORM"></a><a id="printer_change_set_form"></a><dl>
<dt><b>PRINTER_CHANGE_SET_FORM</b></dt>
</dl>
</td>
<td width="60%">
A form was set on the server.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_SET_JOB"></a><a id="printer_change_set_job"></a><dl>
<dt><b>PRINTER_CHANGE_SET_JOB</b></dt>
</dl>
</td>
<td width="60%">
A job was set.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_SET_PRINTER"></a><a id="printer_change_set_printer"></a><dl>
<dt><b>PRINTER_CHANGE_SET_PRINTER</b></dt>
</dl>
</td>
<td width="60%">
A printer was set.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></a><a id="printer_change_set_printer_driver"></a><dl>
<dt><b>PRINTER_CHANGE_SET_PRINTER_DRIVER</b></dt>
</dl>
</td>
<td width="60%">
A printer driver was set.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_WRITE_JOB"></a><a id="printer_change_write_job"></a><dl>
<dt><b>PRINTER_CHANGE_WRITE_JOB</b></dt>
</dl>
</td>
<td width="60%">
Job data was written.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_TIMEOUT"></a><a id="printer_change_timeout"></a><dl>
<dt><b>PRINTER_CHANGE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The job timed out.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_CHANGE_SERVER"></a><a id="printer_change_server"></a><dl>
<dt><b>PRINTER_CHANGE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Windows 7: A change occurred on the server.

</td>
</tr>
</table>
 


### -param pvReserved

TBD


### -param ppPrinterNotifyInfo [out, optional]

A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer. Call the <a href="https://msdn.microsoft.com/e50d4718-3682-486b-9d07-ddddd0b284dc">FreePrinterNotifyInfo</a> function to free the buffer when you are finished with it. This parameter can be <b>NULL</b> if no information is required.

The buffer contains a <a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a> structure, which contains an array of <a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a> structures. Each element of the array contains information about one of the fields specified in the <i>pPrinterNotifyOptions</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> call. Typically, the function provides data only for the fields that changed to cause the most recent notification. However, if the structure pointed to by the <i>pPrinterNotifyOptions</i> parameter specifies <b>PRINTER_NOTIFY_OPTIONS_REFRESH</b>, the function provides data for all monitored fields.

If the <b>PRINTER_NOTIFY_INFO_DISCARDED</b> bit is set in the <b>Flags</b> member of the <a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a> structure, an overflow or error occurred, and notifications may have been lost. In this case, no additional notifications will be sent until you make a second <b>FindNextPrinterChangeNotification</b> call that specifies <b>PRINTER_NOTIFY_OPTIONS_REFRESH</b>.


#### - pPrinterNotifyOptions [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/712c546d-dbb3-4f78-b14e-fbb8619b57f9">PRINTER_NOTIFY_OPTIONS</a> structure. Set the <b>Flags</b> member of this structure to <b>PRINTER_NOTIFY_OPTIONS_REFRESH</b>, to cause the function to return the current data for all monitored printer information fields. The function ignores all other members of the structure. This parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Call the <b>FindNextPrinterChangeNotification</b> function after a wait operation on a notification object created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> has been satisfied. Calling <b>FindNextPrinterChangeNotification</b> lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.

With one exception, do not call the <b>FindNextPrinterChangeNotification</b> function if the change notification object is not in the signaled state. If a wait function returns the value <b>WAIT_TIMEOUT</b>, the change object is not in the signaled state. Call the <b>FindNextPrinterChangeNotification</b> function only if the wait function succeeds without timing out. The exception is when <b>FindNextPrinterChangeNotification</b> is called with the <b>PRINTER_NOTIFY_OPTIONS_REFRESH</b> bit set in the <i>pPrinterNotifyOptions</i> parameter. Note that even when this flag is set, it is still possible for the <b>PRINTER_NOTIFY_INFO_DISCARDED</b> flag to be set in the <i>ppPrinterNotifyInfo</i> parameter.

To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a> , and then calling the <b>FindNextPrinterChangeNotification</b> function to examine the change and reset the notification object.

<b>FindNextPrinterChangeNotification</b> may combine multiple changes to the same printer information field into a single notification. When this occurs, the function typically collapses all changes for the field into a single entry in the array of <a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a> structures in <i>ppPrinterNotifyInfo</i>; the single entry reports only the most current information. However, for some job and printer information fields, the function can return multiple array entries for the same field. In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.

When you no longer need the change notification object, close it by calling the <a href="https://msdn.microsoft.com/2b4758f8-af0a-494b-8f1b-8ea6ee73c79b">FindClosePrinterChangeNotification</a> function.

<div class="alert"><b>Note</b>  In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled. If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server. A machine admin will have to enable exception.</div>
<div> </div>

#### Examples

The following code sample illustrates how you might monitor printer status by using these functions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2b4758f8-af0a-494b-8f1b-8ea6ee73c79b">FindClosePrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/c104fabe-edf5-426e-859b-694811975623">PRINTER_NOTIFY_INFO</a>



<a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a>



<a href="https://msdn.microsoft.com/712c546d-dbb3-4f78-b14e-fbb8619b57f9">PRINTER_NOTIFY_OPTIONS</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

