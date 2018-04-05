---
UID: NF:winspool.GetPrinterDriver2W
title: GetPrinterDriver2W function
author: windows-driver-content
description: The GetPrinterDriver2 function retrieves driver data for the specified printer. If the driver is not installed on the local computer, GetPrinterDriver2 installs it and displays any user interface to the specified window.
old-location: gdi\getprinterdriver2.htm
old-project: printdocs
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 1, 2, 3, 4, 5, 6, 8, GetPrinterDriver2, GetPrinterDriver2 function [Windows GDI], GetPrinterDriver2W, gdi.getprinterdriver2, winspool/GetPrinterDriver2, winspool/GetPrinterDriver2W
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetPrinterDriver2W (Unicode)
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
-	GetPrinterDriver2
-	GetPrinterDriver2W
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPrinterDriver2W function


## -description


The <b>GetPrinterDriver2</b> function retrieves driver data for the specified printer. If the driver is not installed on the local computer, <b>GetPrinterDriver2</b> installs it and displays any user interface to the specified window.


## -parameters




### -param hWnd [in, optional]

A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation. If  the value of this parameter is <b>NULL</b>, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.


### -param hPrinter [in]

A handle to the printer for which the driver data should be retrieved. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pEnvironment [in, optional]

A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the current environment of the calling application and client machine (not of the destination application and print server) is used.


### -param Level [in]

The printer driver structure returned in the <i>pDriverInfo</i> buffer. This parameter can be one of the following values.

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

A pointer to a buffer that receives a structure containing information about the driver, as specified by <i>Level</i>. The buffer must be large enough to store the strings pointed to by the structure members.

To determine the required buffer size, call <b>GetPrinterDriver2</b> with <i>cbBuf</i> set to zero. <b>GetPrinterDriver2</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


### -param cbBuf [in]

The size, in bytes, of the array at which <i>pDriverInfo</i> points.


### -param pcbNeeded [out]

A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if <i>cbBuf</i> is too small.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get the return status, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>, <a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>, <a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>, <a href="https://msdn.microsoft.com/6fb63a9f-5227-46a3-97dc-8de1968e9d63">DRIVER_INFO_5</a>,  <a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff548512">DRIVER_INFO_8</a> structures contain the file name or the full path and file name of the printer driver in the <b>pDriverPath</b> member. An application can use the path and file name to load a printer driver by calling the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function and supplying the path and file name as the single argument.

The ANSI version of this function, <b>GetPrinterDriver2A</b> is not supported and returns <b>ERROR_NOT_SUPPORTED</b>.




## -see-also




<a href="https://msdn.microsoft.com/0f762800-f5a5-40ea-8be1-7fd8bda23788">AddPrinterDriver</a>



<a href="https://msdn.microsoft.com/9435192b-3eba-4937-8cd3-bff4e9eb84d3">DRIVER_INFO_1</a>



<a href="https://msdn.microsoft.com/cca1227d-69b9-44df-8dac-384c2f8843ae">DRIVER_INFO_2</a>



<a href="https://msdn.microsoft.com/ccf87319-0bcf-4f71-8de3-0190459d2b0e">DRIVER_INFO_3</a>



<a href="https://msdn.microsoft.com/63000de6-74e7-4427-98d7-7bbd2dd61080">DRIVER_INFO_4</a>



<a href="https://msdn.microsoft.com/6fb63a9f-5227-46a3-97dc-8de1968e9d63">DRIVER_INFO_5</a>



<a href="https://msdn.microsoft.com/9771cbb5-caaa-4b7d-9a96-d24234440bac">DRIVER_INFO_6</a>



<a href="https://msdn.microsoft.com/fa3d8cf4-70bc-4362-833e-e4217ed5d43b">EnumPrinterDrivers</a>



<a href="https://msdn.microsoft.com/93f859b4-1005-4359-8029-9536d6eeb7e7">GetPrinterDriver</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

