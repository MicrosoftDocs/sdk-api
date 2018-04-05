---
UID: NF:winspool.EnumPrinterDriversA
title: EnumPrinterDriversA function
author: windows-driver-content
description: The EnumPrinterDrivers function enumerates the printer drivers installed on a specified printer server.
old-location: gdi\enumprinterdrivers.htm
old-project: printdocs
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 1, 2, 3, 4, 5, 6, 8, EnumPrinterDrivers, EnumPrinterDrivers function [Windows GDI], EnumPrinterDriversA, EnumPrinterDriversW, _win32_EnumPrinterDrivers, gdi.enumprinterdrivers, winspool/EnumPrinterDrivers, winspool/EnumPrinterDriversA, winspool/EnumPrinterDriversW
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
req.unicode-ansi: EnumPrinterDriversW (Unicode) and EnumPrinterDriversA (ANSI)
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
-	Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
api_name:
-	EnumPrinterDrivers
-	EnumPrinterDriversA
-	EnumPrinterDriversW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPrinterDriversA function


## -description


The <b>EnumPrinterDrivers</b> function enumerates the printer drivers installed on a specified printer server.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.

If <i>pName</i> is <b>NULL</b>, the function enumerates the local printer drivers.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000). If this parameter is <b>NULL</b>, the function uses the current environment of the caller/client (not of the destination/server).

If the <i>pEnvironment</i> string specifies "all", <b>EnumPrinterDrivers</b> enumerates printer drivers for all platforms installed on the specified server.


### -param Level [in]

The type of information structure returned in the <i>pDriverInfo</i> buffer. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/9435192b-3eba-4937-8cd3-bff4e9eb84d3">DRIVER_INFO_1</a>


</td>
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
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/6fb63a9f-5227-46a3-97dc-8de1968e9d63">DRIVER_INFO_5</a>


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
 


### -param pDriverInfo [out]

A pointer to a buffer that receives an array of DRIVER_INFO_* structures, as specified by <i>Level</i>. Each structure contains data that describes an available printer driver. The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.

To determine the required buffer size, call <b>EnumPrinterDrivers</b> with <i>cbBuf</i> set to zero. <b>EnumPrinterDrivers</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pDriverInfo</i>


### -param pcbNeeded [out]

A pointer to a variable that receives the number of bytes copied to the <i>pDriverInfo</i> buffer if the function succeeds. If the buffer is too small, the function fails and the variable receives the number of bytes required.


### -param pcReturned [out]

A pointer to a variable that receives the number of structures returned in the <i>pDriverInfo</i> buffer. This is the number of printer drivers installed on the specified print server.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/9435192b-3eba-4937-8cd3-bff4e9eb84d3">DRIVER_INFO_1</a>



<a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>



<a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>



<a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>



<a href="https://msdn.microsoft.com/6fb63a9f-5227-46a3-97dc-8de1968e9d63">DRIVER_INFO_5</a>



<a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>



<a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

