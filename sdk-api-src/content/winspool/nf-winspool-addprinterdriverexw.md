---
UID: NF:winspool.AddPrinterDriverExW
title: AddPrinterDriverExW function
author: windows-driver-content
description: The AddPrinterDriverEx function installs a local or remote printer driver and links the configuration, data, and driver files.
old-location: gdi\addprinterdriverex.htm
old-project: printdocs
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 2, 3, 4, 6, 8, APD_COPY_ALL_FILES, APD_COPY_FROM_DIRECTORY, APD_COPY_NEW_FILES, APD_STRICT_DOWNGRADE, APD_STRICT_UPGRADE, AddPrinterDriverEx, AddPrinterDriverEx function [Windows GDI], AddPrinterDriverExA, AddPrinterDriverExW, _win32_AddPrinterDriverEx, gdi.addprinterdriverex, winspool/AddPrinterDriverEx, winspool/AddPrinterDriverExA, winspool/AddPrinterDriverExW
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
req.unicode-ansi: AddPrinterDriverExW (Unicode) and AddPrinterDriverExA (ANSI)
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
-	AddPrinterDriverEx
-	AddPrinterDriverExA
-	AddPrinterDriverExW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrinterDriverExW function


## -description


The <b>AddPrinterDriverEx</b> function installs a local or remote printer driver and links the configuration, data, and driver files. Besides having the capabilities of <a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).
<div class="alert"><b>Note</b>  Installing a printer driver without a driver package is no longer recommended. Use <a href="https://msdn.microsoft.com/5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0">InstallPrinterDriverFromPackage</a> instead.</div><div> </div>

## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed. If this parameter is <b>NULL</b>, the function installs the driver on the local computer.


### -param Level [in]

The version of the structure to which <i>pDriverInfo</i> points. This value can be 2, 3, 4, 6, or 8.


### -param lpbDriverInfo

TBD


### -param dwFileCopyFlags [in]

The options for copying the driver files. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="APD_COPY_ALL_FILES"></a><a id="apd_copy_all_files"></a><dl>
<dt><b>APD_COPY_ALL_FILES</b></dt>
</dl>
</td>
<td width="60%">
Add the printer driver and copy all the files in the printer-driver directory. The file time stamps are ignored with this option.

</td>
</tr>
<tr>
<td width="40%"><a id="APD_COPY_FROM_DIRECTORY"></a><a id="apd_copy_from_directory"></a><dl>
<dt><b>APD_COPY_FROM_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">

                 Add the printer driver using the fully qualified file names specified in the <a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a> structure. This flag is ORed in conjunction with one of the other copy flags. If this flag is set, <b>AddPrinterDriverEx</b> will fail if the files do not exist where they are specified to exist by the <b>DRIVER_INFO_6</b> structure. The files do not need to be copied to the system's printer-driver directory. See the Remarks.

<b>Windows 2000:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="APD_COPY_NEW_FILES"></a><a id="apd_copy_new_files"></a><dl>
<dt><b>APD_COPY_NEW_FILES</b></dt>
</dl>
</td>
<td width="60%">
Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use. This flag emulates the behavior of <a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="APD_STRICT_DOWNGRADE"></a><a id="apd_strict_downgrade"></a><dl>
<dt><b>APD_STRICT_DOWNGRADE</b></dt>
</dl>
</td>
<td width="60%">
Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.

</td>
</tr>
<tr>
<td width="40%"><a id="APD_STRICT_UPGRADE"></a><a id="apd_strict_upgrade"></a><dl>
<dt><b>APD_STRICT_UPGRADE</b></dt>
</dl>
</td>
<td width="60%">
Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.

</td>
</tr>
</table>
 


#### - pDriverInfo [in, out]

A pointer to a structure containing printer driver information. It can be one of the following.

<table>
<tr>
<th>Value of Level</th>
<th>DRIVER_INFO_* Structure</th>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>


</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>


</td>
</tr>
<tr>
<td width="40%"><a id="6"></a><dl>
<dt><b>6</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>


</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff548512">DRIVER_INFO_8</a>


</td>
</tr>
</table>
 

If the <b>pEnvironment</b> member of the structure pointed to by <i>pDriverInfo</i> is <b>NULL</b>, the function uses the current environment of the caller/client, not the environment of the destination/server.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 


               If the printer driver is known to have problems working with the operating system, <b>AddPrinterDriverEx</b> will fail with one of the following error codes:

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>
<tr>
<td>ERROR_PRINTER_DRIVER_BLOCKED</td>
<td>The driver does not work on the operating system.</td>
</tr>
<tr>
<td>ERROR_PRINTER_DRIVER_WARNED</td>
<td>The driver is unreliable on the operating system. However, if APD_INSTALL_WARNED_DRIVER is specified, the driver is installed and no warning is given.</td>
</tr>
</table>
 

For more information, see the Remarks.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.

Before calling the <b>AddPrinterDriverEx</b> function, all files required by the driver must be copied to the system's printer-driver directory. To retrieve the name of this directory, call the <a href="https://msdn.microsoft.com/69c9cc87-d7e3-496a-b631-b3ae30cdb3fd">GetPrinterDriverDirectory</a> function.

To determine which printer drivers are currently installed, call the <a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a> function.

If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER_EVENT_INITIALIZE, Level, DRIVER_INFO_*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver. For more information about <b>DrvDriverEvent</b>, see the Microsoft Windows Driver Development Kit (DDK)


         The driver should not use a UI call during the call to <b>DrvDriverEvent</b>. To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer. For more information about VendorSetup, see the DDK.


         The files that are referenced in the <a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a> structure must be local to the machine from which the call is made. A file name can be a UNC name as long as the UNC name is the local machine.




## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>



<a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>



<a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>



<a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>



<a href="https://msdn.microsoft.com/1a3d7c7f-1d45-4877-a8f7-a77f40e3c319">DeletePrinterDriverEx</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/69c9cc87-d7e3-496a-b631-b3ae30cdb3fd">GetPrinterDriverDirectory</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

