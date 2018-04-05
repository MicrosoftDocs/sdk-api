---
UID: NF:winspool.SetPortA
title: SetPortA function
author: windows-driver-content
description: The SetPort function sets the status associated with a printer port.
old-location: gdi\setport.htm
old-project: printdocs
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetPort, SetPort function [Windows GDI], SetPortA, SetPortW, _win32_SetPort, gdi.setport, winspool/SetPort, winspool/SetPortA, winspool/SetPortW
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
req.unicode-ansi: SetPortW (Unicode) and SetPortA (ANSI)
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
-	SetPort
-	SetPortA
-	SetPortW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetPortA function


## -description


The <b>SetPort</b> function sets the status associated with a printer port.


## -parameters




### -param pName [in]

Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected. Set this parameter to <b>NULL</b> if the port is on the local machine.


### -param pPortName [in]

Pointer to a zero-terminated string that specifies the name of the printer port.


### -param dwLevel [in]

Specifies the type of structure pointed to by the <i>pPortInfo</i> parameter.

This value must be 3, which corresponds to a <a href="https://msdn.microsoft.com/0939353f-284b-4dbb-89a2-04918c934430">PORT_INFO_3</a> data structure.


### -param pPortInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/0939353f-284b-4dbb-89a2-04918c934430">PORT_INFO_3</a> structure that contains the port status information to set.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The caller of the <b>SetPort</b> function must be executing as an Administrator. Additionally, if the caller is a Port Monitor or Language Monitor, it must call <a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a> to cease impersonation before it calls <b>SetPort</b>.

All programs that call <b>SetPort</b> must have SERVER_ACCESS_ADMINISTER access to the server to which the port is connected.


When you set a printer port status value with the severity value PORT_STATUS_TYPE_ERROR, the print spooler stops sending jobs to the port. The print spooler resumes sending jobs to the port when the port status is cleared by another call to <b>SetPort</b>.




## -see-also




<a href="https://msdn.microsoft.com/0939353f-284b-4dbb-89a2-04918c934430">PORT_INFO_3</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

