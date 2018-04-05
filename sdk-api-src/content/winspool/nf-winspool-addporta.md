---
UID: NF:winspool.AddPortA
title: AddPortA function
author: windows-driver-content
description: The AddPort function adds the name of a port to the list of supported ports. The AddPort function is exported by the port monitor.
old-location: gdi\addport.htm
old-project: printdocs
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddPort, AddPort function [Windows GDI], AddPortA, AddPortW, _win32_AddPort, gdi.addport, winspool/AddPort, winspool/AddPortA, winspool/AddPortW
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
req.unicode-ansi: AddPortW (Unicode) and AddPortA (ANSI)
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
-	AddPort
-	AddPortA
-	AddPortW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddPortA function


## -description


The <b>AddPort</b> function adds the name of a port to the list of supported ports. The <b>AddPort</b> function is exported by the port monitor.


## -parameters




### -param pName [in]

A pointer to a zero-terminated string that specifies the name of the server to which the port is connected. If this parameter is <b>NULL</b>, the port is local.


### -param hWnd [in]

A handle to the parent window of the <b>AddPort</b> dialog box.


### -param pMonitorName [in]

A pointer to a zero-terminated string that specifies the monitor associated with the port.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <b>AddPort</b> function browses the network to find existing ports, and displays a dialog box for the user. The <b>AddPort</b> function should validate the port name entered by the user by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a> to ensure that no duplicate names exist.

The caller of the <b>AddPort</b> function must have SERVER_ACCESS_ADMINISTER access to the server to which the port is connected.

To add a port without displaying a dialog box, call the <b>XcvData</b> function instead of <b>AddPort</b>. For more information about <b>XcvData</b>, see the Microsoft Windows Driver Development Kit (DDK).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547427">DeletePort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/1b80ad93-aaa1-41ed-a668-a944fa62c3eb">SetPort</a>
 

 

