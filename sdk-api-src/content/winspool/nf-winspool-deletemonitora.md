---
UID: NF:winspool.DeleteMonitorA
title: DeleteMonitorA function
author: windows-driver-content
description: The DeleteMonitor function removes a port monitor added by the AddMonitor function.
old-location: gdi\deletemonitor.htm
old-project: printdocs
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeleteMonitor, DeleteMonitor function [Windows GDI], DeleteMonitorA, DeleteMonitorW, _win32_DeleteMonitor, gdi.deletemonitor, winspool/DeleteMonitor, winspool/DeleteMonitorA, winspool/DeleteMonitorW
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
req.unicode-ansi: DeleteMonitorW (Unicode) and DeleteMonitorA (ANSI)
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
-	DeleteMonitor
-	DeleteMonitorA
-	DeleteMonitorW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeleteMonitorA function


## -description


The <b>DeleteMonitor</b> function removes a port monitor added by the <a href="https://msdn.microsoft.com/6a556422-5360-42d2-b177-dba0498c06d8">AddMonitor</a> function.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed. If this parameter is <b>NULL</b>, the port monitor is removed locally.


### -param pEnvironment [in]

A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64). If this parameter is <b>NULL</b>, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).
			 


### -param pMonitorName [in]

A pointer to a null-terminated string that specifies the name of the monitor to be removed.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller must have <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLoadDriverPrivilege</a>.




## -see-also




<a href="https://msdn.microsoft.com/6a556422-5360-42d2-b177-dba0498c06d8">AddMonitor</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

