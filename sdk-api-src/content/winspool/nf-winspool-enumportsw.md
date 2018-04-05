---
UID: NF:winspool.EnumPortsW
title: EnumPortsW function
author: windows-driver-content
description: The EnumPorts function enumerates the ports that are available for printing on a specified server.
old-location: gdi\enumports.htm
old-project: printdocs
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumPorts, EnumPorts function [Windows GDI], EnumPortsA, EnumPortsW, _win32_EnumPorts, gdi.enumports, winspool/EnumPorts, winspool/EnumPortsA, winspool/EnumPortsW
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
req.unicode-ansi: EnumPortsW (Unicode) and EnumPortsA (ANSI)
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
-	EnumPorts
-	EnumPortsA
-	EnumPortsW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumPortsW function


## -description


The <b>EnumPorts</b> function enumerates the ports that are available for printing on a specified server.


## -parameters




### -param pName [in]

A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.

If <i>pName</i> is <b>NULL</b>, the function enumerates the local machine's printer ports.


### -param Level [in]

The type of information returned in the <i>pPorts</i> buffer. If <i>Level</i> is 1, <i>pPorts</i> receives an array of <a href="https://msdn.microsoft.com/e474fe9c-e554-406a-a5bf-de07f9a72b32">PORT_INFO_1</a> structures. If <i>Level</i> is 2, <i>pPorts</i> receives an array of <a href="https://msdn.microsoft.com/93675294-61d4-40e4-b84c-f252978e0285">PORT_INFO_2</a> structures.


### -param pPort

TBD


### -param cbBuf [in]

The size, in bytes, of the buffer pointed to by <i>pPorts</i>.


### -param pcbNeeded [out]

A pointer to a variable that receives the number of bytes copied to the <i>pPorts</i> buffer. If the buffer is too small, the function fails and the variable receives the number of bytes required.


### -param pcReturned [out]

A pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/e474fe9c-e554-406a-a5bf-de07f9a72b32">PORT_INFO_1</a> or <a href="https://msdn.microsoft.com/93675294-61d4-40e4-b84c-f252978e0285">PORT_INFO_2</a> structures returned in the <i>pPorts</i> buffer. This is the number of printer ports that are available on the specified server.


#### - pPorts [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/e474fe9c-e554-406a-a5bf-de07f9a72b32">PORT_INFO_1</a> or <a href="https://msdn.microsoft.com/93675294-61d4-40e4-b84c-f252978e0285">PORT_INFO_2</a> structures. Each structure contains data that describes an available printer port. The buffer must be large enough to store the strings pointed to by the structure members.

To determine the required buffer size, call <b>EnumPorts</b> with <i>cbBuf</i> set to zero. <b>EnumPorts</b> fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>pcbNeeded</i> parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The <b>EnumPorts</b> function can succeed even if the server specified by <i>pName</i> does not have a printer defined.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545022">AddPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547427">DeletePort</a>



<a href="https://msdn.microsoft.com/e474fe9c-e554-406a-a5bf-de07f9a72b32">PORT_INFO_1</a>



<a href="https://msdn.microsoft.com/93675294-61d4-40e4-b84c-f252978e0285">PORT_INFO_2</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

