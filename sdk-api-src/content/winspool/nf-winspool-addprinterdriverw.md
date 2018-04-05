---
UID: NF:winspool.AddPrinterDriverW
title: AddPrinterDriverW function
author: windows-driver-content
description: The AddPrinterDriver function installs a local or remote printer driver and associates the configuration, data, and driver files.
old-location: gdi\addprinterdriver.htm
old-project: printdocs
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddPrinterDriver, AddPrinterDriver function [Windows GDI], AddPrinterDriverA, AddPrinterDriverW, _win32_AddPrinterDriver, gdi.addprinterdriver, winspool/AddPrinterDriver, winspool/AddPrinterDriverA, winspool/AddPrinterDriverW
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
req.unicode-ansi: AddPrinterDriverW (Unicode) and AddPrinterDriverA (ANSI)
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
-	AddPrinterDriver
-	AddPrinterDriverA
-	AddPrinterDriverW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPrinterDriverW function


## -description


The <b>AddPrinterDriver</b> function installs a local or remote printer driver and associates the configuration, data, and driver files.

For more flexibility in installing or upgrading printer drivers, use the <a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).
<div class="alert"><b>Note</b>  Installing a printer driver without a driver package is no longer recommended. Use <a href="https://msdn.microsoft.com/5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0">InstallPrinterDriverFromPackage</a> instead.</div><div> </div>

## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.

If <i>pName</i> is <b>NULL</b>, the driver will be installed locally.


### -param Level [in]

The version of the structure to which <i>pDriverInfo</i> points.

This value can be 2, 3, 4, 6, or 8.


### -param pDriverInfo [in]

A pointer to a structure containing printer driver information. This depends on the value of <i>Level</i>.

<table>
<tr>
<th>Value</th>
<th>Printer Drive Structure</th>
</tr>
<tr>
<td>2</td>
<td>
<a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>
</td>
</tr>
<tr>
<td>3</td>
<td>
<a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>
</td>
</tr>
<tr>
<td>4</td>
<td>
<a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>
</td>
</tr>
<tr>
<td>6</td>
<td>
<a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>
</td>
</tr>
<tr>
<td>8</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff548512">DRIVER_INFO_8</a>
</td>
</tr>
</table>
 

If the <b>pEnvironment</b> member of the structure pointed to by <i>pDriverInfo</i> is <b>NULL</b>, the current environment of the caller/client (not of the destination/server) is used.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.

Before an application calls the <b>AddPrinterDriver</b> function, all files required by the driver must be copied to the system's printer-driver directory. An application can retrieve the name of this directory by calling the <a href="https://msdn.microsoft.com/69c9cc87-d7e3-496a-b631-b3ae30cdb3fd">GetPrinterDriverDirectory</a> function.

An application can determine which printer drivers are currently installed by calling the <a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a> function.




## -see-also




<a href="https://msdn.microsoft.com/472adb7d-39cc-4c76-b96c-610ff9d276ad">AddPrinterDriverEx</a>



<a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>



<a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>



<a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>



<a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/69c9cc87-d7e3-496a-b631-b3ae30cdb3fd">GetPrinterDriverDirectory</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

