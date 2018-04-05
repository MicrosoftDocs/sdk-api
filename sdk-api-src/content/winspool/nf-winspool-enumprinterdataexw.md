---
UID: NF:winspool.EnumPrinterDataExW
title: EnumPrinterDataExW function
author: windows-driver-content
description: The EnumPrinterDataEx function enumerates all value names and data for a specified printer and key.
old-location: gdi\enumprinterdataex.htm
old-project: printdocs
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumPrinterDataEx, EnumPrinterDataEx function [Windows GDI], EnumPrinterDataExA, EnumPrinterDataExW, _win32_EnumPrinterDataEx, gdi.enumprinterdataex, winspool/EnumPrinterDataEx, winspool/EnumPrinterDataExA, winspool/EnumPrinterDataExW
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
req.unicode-ansi: EnumPrinterDataExW (Unicode) and EnumPrinterDataExA (ANSI)
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
-	EnumPrinterDataEx
-	EnumPrinterDataExA
-	EnumPrinterDataExW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPrinterDataExW function


## -description


The <b>EnumPrinterDataEx</b> function enumerates all value names and data for a specified printer and key.

Printer data is stored in the registry. While enumerating printer data, do not call registry functions that might change the data.


## -parameters




### -param hPrinter [in]

A handle to the printer for which the function retrieves configuration data. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pKeyName [in]

A pointer to a null-terminated string that specifies the key containing the values to enumerate. Use the backslash ( \ ) character as a delimiter to specify a path with one or more subkeys. <b>EnumPrinterDataEx</b> enumerates all values of the key, but does not enumerate values of subkeys of the specified key. Use the <a href="https://msdn.microsoft.com/721b1d23-a594-4439-b8f9-9b11be5fe874">EnumPrinterKey</a> function to enumerate subkeys.

If <i>pKeyName</i> is <b>NULL</b> or an empty string, <b>EnumPrinterDataEx</b> returns ERROR_INVALID_PARAMETER.


### -param pEnumValues [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/87eb1452-0d9d-46bd-8af8-0542a11a929b">PRINTER_ENUM_VALUES</a> structures. Each structure contains the value name, type, data, and sizes of a value under the key.


### -param cbEnumValues [in]

The size, in bytes, of the buffer pointed to by <i>pcbEnumValues</i>. If you set <i>cbEnumValues</i> to zero, the <i>pcbEnumValues</i> parameter returns the required buffer size.


### -param pcbEnumValues [out]

A pointer to a variable that receives the size, in bytes, of the retrieved configuration data. If the buffer size specified by <i>cbEnumValues</i> is too small, the function returns ERROR_MORE_DATA and <i>pcbEnumValues</i> indicates the required buffer size.


### -param pnEnumValues [out]

A pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/87eb1452-0d9d-46bd-8af8-0542a11a929b">PRINTER_ENUM_VALUES</a> structures returned in <i>pEnumValues</i>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a system error code.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>EnumPrinterDataEx</b> retrieves printer configuration data set by the <a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a> and <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55">DeletePrinterDataEx</a>



<a href="https://msdn.microsoft.com/721b1d23-a594-4439-b8f9-9b11be5fe874">EnumPrinterKey</a>



<a href="https://msdn.microsoft.com/5d9183a7-97cc-46de-848e-e37ce51396eb">GetPrinterDataEx</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/87eb1452-0d9d-46bd-8af8-0542a11a929b">PRINTER_ENUM_VALUES</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a>



<a href="https://msdn.microsoft.com/b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1">SetPrinterDataEx</a>
 

 

