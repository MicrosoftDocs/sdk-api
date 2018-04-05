---
UID: NF:winspool.EnumMonitorsW
title: EnumMonitorsW function
author: windows-driver-content
description: The EnumMonitors function retrieves information about the port monitors installed on the specified server.
old-location: gdi\enummonitors.htm
old-project: printdocs
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumMonitors, EnumMonitors function [Windows GDI], EnumMonitorsA, EnumMonitorsW, _win32_EnumMonitors, gdi.enummonitors, winspool/EnumMonitors, winspool/EnumMonitorsA, winspool/EnumMonitorsW
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
req.unicode-ansi: EnumMonitorsW (Unicode) and EnumMonitorsA (ANSI)
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
-	EnumMonitors
-	EnumMonitorsA
-	EnumMonitorsW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumMonitorsW function


## -description


The <b>EnumMonitors</b> function retrieves information about the port monitors installed on the specified server.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the monitors reside. If this parameter is <b>NULL</b>, the local monitors are enumerated.


### -param Level [in]

The version of the structure pointed to by <i>pMonitors</i>.


             This value can be 1 or 2.


### -param pMonitor

TBD


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pMonitors</i>.


### -param pcbNeeded [out]

A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if <i>cbBuf</i> is too small.


### -param pcReturned [out]

A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by <i>pMonitors</i>.


#### - pMonitors [out]

A pointer to a buffer that receives an array of structures. The buffer must be large enough to store the strings referenced by the structure members.

To determine the required buffer size, call <b>EnumMonitors</b> with <i>cbBuf</i> set to zero. <b>EnumMonitors</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


             The buffer receives an array of <a href="https://msdn.microsoft.com/7a4660bd-5df8-49dd-92f6-9574f451f10d">MONITOR_INFO_1</a> structures if <i>Level</i> is 1, or <a href="https://msdn.microsoft.com/4dd1ca15-6983-403e-8159-1a6d35a88162">MONITOR_INFO_2</a> structures if <i>Level</i> is 2.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a4660bd-5df8-49dd-92f6-9574f451f10d">MONITOR_INFO_1</a>



<a href="https://msdn.microsoft.com/4dd1ca15-6983-403e-8159-1a6d35a88162">MONITOR_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

