---
UID: NF:winspool.EnumPrinterDataW
title: EnumPrinterDataW function
author: windows-driver-content
description: The EnumPrinterData function enumerates configuration data for a specified printer.
old-location: gdi\enumprinterdata.htm
old-project: printdocs
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumPrinterData, EnumPrinterData function [Windows GDI], EnumPrinterDataA, EnumPrinterDataW, _win32_EnumPrinterData, gdi.enumprinterdata, winspool/EnumPrinterData, winspool/EnumPrinterDataA, winspool/EnumPrinterDataW
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
req.unicode-ansi: EnumPrinterDataW (Unicode) and EnumPrinterDataA (ANSI)
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
-	EnumPrinterData
-	EnumPrinterDataA
-	EnumPrinterDataW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPrinterDataW function


## -description


The <b>EnumPrinterData</b> function enumerates configuration data for a specified printer.

To retrieve the configuration data in a single call, use the <a href="https://msdn.microsoft.com/bc5ecc46-24a4-4b54-9431-0eaf6446e2d6">EnumPrinterDataEx</a> function.


## -parameters




### -param hPrinter [in]

A handle to the printer whose configuration data is to be obtained. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param dwIndex [in]

An index value that specifies the configuration data value to retrieve.

Set this parameter to zero for the first call to <b>EnumPrinterData</b> for a specified printer handle. Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR_NO_MORE_ITEMS. See the following Remarks section for further information.

If you use the technique mentioned in the descriptions of the <i>cbValueName</i> and <i>cbData</i> parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to <b>EnumPrinterData</b> for a specified printer handle, the value of <i>dwIndex</i> does not matter for that call. Set <i>dwIndex</i> to zero in the next call to <b>EnumPrinterData</b> to start the actual enumeration process.

Configuration data values are not ordered. New values will have an arbitrary index. This means that the <b>EnumPrinterData</b> function may return values in any order.


### -param pValueName [out]

A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.


### -param cbValueName [in]

The size, in bytes, of the buffer pointed to by <i>pValueName</i>.

If you want to have the operating system supply an adequate buffer size, set both this parameter and the <i>cbData</i> parameter to zero for the first call to <b>EnumPrinterData</b> for a specified printer handle. When the function returns, the variable pointed to by <i>pcbValueName</i> will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.


### -param pcbValueName [out]

A pointer to a variable that receives the number of bytes stored into the buffer pointed to by <i>pValueName</i>.


### -param pType [out]

A pointer to a variable that receives a code indicating the type of data stored in the specified value. For a list of the possible type codes, see <a href="https://msdn.microsoft.com/5fd828d6-4d62-4823-a2f1-15782b5cd28c">Registry Value Types</a>. The <i>pType</i> parameter can be <b>NULL</b> if the type code is not required.


### -param pData [out]

A pointer to a buffer that receives the configuration data value.

This parameter can be <b>NULL</b> if the configuration data value is not required.


### -param cbData [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.

If you want to have the operating system supply an adequate buffer size, set both this parameter and the <i>cbValueName</i> parameter to zero for the first call to <b>EnumPrinterData</b> for a specified printer handle. When the function returns, the variable pointed to by <i>pcbData</i> will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.


### -param pcbData [out]

A pointer to a variable that receives the number of bytes stored into the buffer pointed to by <i>pData</i>.

This parameter can be <b>NULL</b> if <i>pData</i> is <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a system error code.

The function returns ERROR_NO_MORE_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>EnumPrinterData</b> retrieves printer configuration data set by the <a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a> function. A printer's configuration data consists of a set of named and typed values. The <b>EnumPrinterData</b> function obtains one of these values, and its name and a type code, each time you call it. Call the <b>EnumPrinterData</b> function several times in succession to obtain all of a printer's configuration data values.

Printer configuration data is stored in the registry. While enumerating printer configuration data, you should avoid calling registry functions that might change that data.

If you want to have the operating system supply an adequate buffer size, first call <b>EnumPrinterData</b> with both the <i>cbValueName</i> and <i>cbData</i> parameters set to zero, as noted earlier in the Parameters section. The value of <i>dwIndex</i> does not matter for this call. When the function returns, *<i>pcbValueName</i> and *<i>pcbData</i> will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values. On the next call, allocate value name and data buffers, set <i>cbValueName</i> and <i>cbData</i> to the sizes in bytes of the allocated buffers, and set <i>dwIndex</i> to zero. Thereafter, continue to call the <b>EnumPrinterData</b> function, incrementing <i>dwIndex</i> by one each time, until the function returns ERROR_NO_MORE_ITEMS.




## -see-also




<a href="https://msdn.microsoft.com/03c0bd75-d6de-46e3-b8e9-5a55df5135ea">DeletePrinterData</a>



<a href="https://msdn.microsoft.com/bc5ecc46-24a4-4b54-9431-0eaf6446e2d6">EnumPrinterDataEx</a>



<a href="https://msdn.microsoft.com/b5a44b27-a4aa-4e58-9a64-05be87d12ab5">GetPrinterData</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>



<a href="https://msdn.microsoft.com/16072de9-98fb-4ada-8216-180b64cf44c8">SetPrinterData</a>
 

 

