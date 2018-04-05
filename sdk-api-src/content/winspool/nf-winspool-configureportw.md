---
UID: NF:winspool.ConfigurePortW
title: ConfigurePortW function
author: windows-driver-content
description: The ConfigurePort function displays the port-configuration dialog box for a port on the specified server.
old-location: gdi\configureport.htm
old-project: printdocs
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ConfigurePort, ConfigurePort function [Windows GDI], ConfigurePortA, ConfigurePortW, _win32_ConfigurePort, gdi.configureport, winspool/ConfigurePort, winspool/ConfigurePortA, winspool/ConfigurePortW
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
req.unicode-ansi: ConfigurePortW (Unicode) and ConfigurePortA (ANSI)
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
-	ConfigurePort
-	ConfigurePortA
-	ConfigurePortW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ConfigurePortW function


## -description


The <b>ConfigurePort</b> function displays the port-configuration dialog box for a port on the specified server.


## -parameters




### -param pName [in]

Pointer to a null-terminated string that specifies the name of the server on which the specified port exists. If this parameter is <b>NULL</b>, the port is local.


### -param hWnd [in]

Handle to the parent window of the port-configuration dialog box.


### -param pPortName [in]

Pointer to a null-terminated string that specifies the name of the port to be configured.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
Before calling the <b>ConfigurePort</b> function, an application should call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a> function to determine valid port names.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

