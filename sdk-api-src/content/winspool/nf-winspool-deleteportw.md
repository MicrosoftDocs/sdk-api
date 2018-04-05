---
UID: NF:winspool.DeletePortW
title: DeletePortW function
author: windows-driver-content
description: The DeletePort function displays a dialog box that allows the user to delete a port name.
old-location: gdi\deleteport.htm
old-project: printdocs
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeletePort, DeletePort function [Windows GDI], DeletePortA, DeletePortW, _win32_DeletePort, gdi.deleteport, winspool/DeletePort, winspool/DeletePortA, winspool/DeletePortW
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
req.unicode-ansi: DeletePortW (Unicode) and DeletePortA (ANSI)
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
-	DeletePort
-	DeletePortA
-	DeletePortW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeletePortW function


## -description


The <b>DeletePort</b> function displays a dialog box that allows the user to delete a port name.


## -parameters




### -param pName [in]

A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted. If this parameter is <b>NULL</b>, a local port is deleted.


### -param hWnd [in]

A handle to the parent window of the port-deletion dialog box.


### -param pPortName [in]

A pointer to a zero-terminated string that specifies the name of the port that should be deleted.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
An application can retrieve the names of valid ports by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a> function.

The <b>DeletePort</b> function returns an error if a printer is currently connected to the specified port.

The caller of the <b>DeletePort</b> function must have SERVER_ACCESS_ADMINISTER access to the server to which the port is connected.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545022">AddPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

