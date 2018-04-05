---
UID: NF:winspool.AddMonitorW
title: AddMonitorW function
author: windows-driver-content
description: The AddMonitor function installs a local port monitor and links the configuration, data, and monitor files.
old-location: gdi\addmonitor.htm
old-project: printdocs
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddMonitor, AddMonitor function [Windows GDI], AddMonitorA, AddMonitorW, _win32_AddMonitor, gdi.addmonitor, winspool/AddMonitor, winspool/AddMonitorA, winspool/AddMonitorW
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
req.unicode-ansi: AddMonitorW (Unicode) and AddMonitorA (ANSI)
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
-	AddMonitor
-	AddMonitorA
-	AddMonitorW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AddMonitorW function


## -description


The <b>AddMonitor</b> function installs a local port monitor and links the configuration, data, and monitor files.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed. For systems that support only local installation of monitors, this string should be <b>NULL</b>.


### -param Level [in]

The version of the structure to which <i>pMonitors</i> points. This value must be 2.


### -param pMonitors [in]

A  pointer to a <a href="https://msdn.microsoft.com/4dd1ca15-6983-403e-8159-1a6d35a88162">MONITOR_INFO_2</a> structure. If the <b>pEnvironment</b> member of the <i>pMonitors</i> structure is <b>NULL</b>, the current environment of the caller (client), not of the destination (server), is used.

Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.

Before an application calls the <b>AddMonitor</b> function, all files required by the monitor must be copied to the SYSTEM32 directory.

To determine the port monitors that are currently installed, call the <a href="https://msdn.microsoft.com/4d4fbed2-193f-426c-8463-eeb6b1eaf316">EnumMonitors</a> function.

To remove a monitor added by <b>AddMonitor</b>, call the <a href="https://msdn.microsoft.com/32548d4f-830a-471d-8a72-c0f62f43ffa2">DeleteMonitor</a> function.




## -see-also




<a href="https://msdn.microsoft.com/32548d4f-830a-471d-8a72-c0f62f43ffa2">DeleteMonitor</a>



<a href="https://msdn.microsoft.com/4d4fbed2-193f-426c-8463-eeb6b1eaf316">EnumMonitors</a>



<a href="https://msdn.microsoft.com/4dd1ca15-6983-403e-8159-1a6d35a88162">MONITOR_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

