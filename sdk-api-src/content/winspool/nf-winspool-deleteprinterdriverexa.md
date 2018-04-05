---
UID: NF:winspool.DeletePrinterDriverExA
title: DeletePrinterDriverExA function
author: windows-driver-content
description: The DeletePrinterDriverEx function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver. This function can also delete specific versions of the driver.
old-location: gdi\deleteprinterdriverex.htm
old-project: printdocs
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DPD_DELETE_ALL_FILES, DPD_DELETE_SPECIFIC_VERSION, DPD_DELETE_UNUSED_FILES, DeletePrinterDriverEx, DeletePrinterDriverEx function [Windows GDI], DeletePrinterDriverExA, DeletePrinterDriverExW, _win32_DeletePrinterDriverEx, gdi.deleteprinterdriverex, winspool/DeletePrinterDriverEx, winspool/DeletePrinterDriverExA, winspool/DeletePrinterDriverExW
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
req.unicode-ansi: DeletePrinterDriverExW (Unicode) and DeletePrinterDriverExA (ANSI)
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
-	DeletePrinterDriverEx
-	DeletePrinterDriverExA
-	DeletePrinterDriverExW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePrinterDriverExA function


## -description


The <b>DeletePrinterDriverEx</b> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver. This function can also delete specific versions of the driver.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted. If this parameter is <b>NULL</b>, the function deletes the printer-driver from the local computer.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).


### -param pDriverName [in]

A pointer to a null-terminated string specifying the name of the driver to delete.


### -param dwDeleteFlag [in]

The options for deleting files and versions of the driver. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DPD_DELETE_SPECIFIC_VERSION"></a><a id="dpd_delete_specific_version"></a><dl>
<dt><b>DPD_DELETE_SPECIFIC_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Deletes the version specified in <i>dwVersionFlag</i>. This does not ensure that the driver will be removed from the list of supported drivers for the server.

</td>
</tr>
<tr>
<td width="40%"><a id="DPD_DELETE_UNUSED_FILES"></a><a id="dpd_delete_unused_files"></a><dl>
<dt><b>DPD_DELETE_UNUSED_FILES</b></dt>
</dl>
</td>
<td width="60%">
Removes any unused driver files.

</td>
</tr>
<tr>
<td width="40%"><a id="DPD_DELETE_ALL_FILES"></a><a id="dpd_delete_all_files"></a><dl>
<dt><b>DPD_DELETE_ALL_FILES</b></dt>
</dl>
</td>
<td width="60%">
Deletes the driver only if all its associated files can be removed. The delete operation fails if any of the driver's files are being used by some other installed driver.

</td>
</tr>
</table>
 

If DPD_DELETE_SPECIFIC_VERSION is not specified, the function deletes all versions of the driver if none of them is in use. If neither DPD_DELETE_UNUSED_FILES nor DPD_DELETE_ALL_FILES is specified, the function does not delete driver files.


### -param dwVersionFlag [in]

The version of the driver to be deleted. This parameter can be 0, 1, 2 or 3. This parameter is used only if <i>dwDeleteFlag</i> includes the DPD_DELETE_SPECIFIC_VERSION flag.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Before the function deletes the driver files, it calls the driver's <b>DrvDriverEvent</b> function, allowing the driver to remove any private files that are not used. For more information about <b>DrvDriverEvent</b>, see the Microsoft Windows Driver Development Kit (DDK).

If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.

Before calling <b>DeletePrinterDriverEx</b>, you must delete all printer objects that use the printer driver.




## -see-also




<a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

