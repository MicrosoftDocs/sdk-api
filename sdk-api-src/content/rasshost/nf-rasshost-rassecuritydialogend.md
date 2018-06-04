---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RasSecurityDialogEnd function


## -description


The 
<b>RasSecurityDialogEnd</b> function is a third-party RAS security DLL entry point that the RAS server calls to terminate an authentication transaction.
<div class="alert"><b>Note</b>  Windows Server 2008, 
  Windows Server 2003,
  Windows 2000 Server, and
  Windows NT Server 4.0 currently provide RAS security host support for serial devices only. Other types of connections, such as Integrated Services Digital Network (ISDN) or virtual private network (VPN) connections, are not supported.</div><div> </div>

## -parameters




### -param hPort [in]

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> call for this authentication transaction.


## -returns



If the security DLL returns <b>NO_ERROR</b>, the RAS server does not terminate the authentication transaction. In this case, the security DLL must later call the 
<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a> function when it is ready to terminate.

If the security DLL returns a nonzero error code, the RAS server terminates the authentication transaction. In this case, the security DLL does not need to make another 
<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a> call. Return an error code defined in Winerror.h or Raserror.h, such as <b>ERROR_PORT_DISCONNECTED</b>.




## -remarks



When a security DLL has finished authenticating the remote user, it calls the 
<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a> function. The RAS server then performs a cleanup sequence that includes a call to the DLL's 
<b>RasSecurityDialogEnd</b> function. This gives the security DLL an opportunity to perform any necessary cleanup. To terminate the authentication transaction, 
<b>RasSecurityDialogEnd</b> must return a nonzero error code.

The RAS server may also call 
<b>RasSecurityDialogEnd</b> if it needs to abnormally terminate the authentication transaction before the security DLL calls 
<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a>. In this case, the security DLL should terminate the worker thread associated with the <i>hPort</i> port handle, and perform any other necessary cleanup. If 
<b>RasSecurityDialogEnd</b> returns a nonzero value, the security DLL does not need to call 
<b>RasSecurityDialogComplete</b>.

For both normal and abnormal termination, the 
<b>RasSecurityDialogEnd</b> function returns NO_ERROR to delay the termination. If it does so, it must later call 
<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a> when it is ready to terminate.




## -see-also




<a href="https://msdn.microsoft.com/44c000d7-2bb6-4fd8-ac5f-9d3850d857a0">RAS Server Administration Functions</a>



<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a>



<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>
 

 

