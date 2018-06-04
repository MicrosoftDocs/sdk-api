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

# AbortSystemShutdownW function


## -description


Stops a system shutdown that has been initiated.


## -parameters




### -param lpMachineName [in, optional]

The network name of the computer where the shutdown is to be stopped. If <i>lpMachineName</i> is <b>NULL</b> or an empty string, the function stops the shutdown on the local computer.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/cad54fea-7f59-438c-83ac-f0160d81496b">InitiateSystemShutdown</a> and 
<a href="https://msdn.microsoft.com/4536cf76-7669-42b1-8c44-9f5e368424cc">InitiateSystemShutdownEx</a> functions display a dialog box that notifies the user that the system is shutting down. During the shutdown time-out period, the 
<b>AbortSystemShutdown</b> function can prevent the system from shutting down.

<b>Windows Server 2003 and Windows XP with SP1:  </b>If the computer to be shut down is a Terminal Services server, the system displays a dialog box to all local and remote users warning them that shutdown has been initiated. If shutdown is prevented by 
<b>AbortSystemShutdown</b>, the system displays dialog box to the users informing them that the server is no longer shutting down.

To stop the local computer from shutting down, the calling process must have the SE_SHUTDOWN_NAME privilege. To stop a remote computer from shutting down, the calling process must have the SE_REMOTE_SHUTDOWN_NAME privilege on the remote computer. By default, users can enable the SE_SHUTDOWN_NAME privilege on the computer they are logged onto, and administrators can enable the SE_REMOTE_SHUTDOWN_NAME privilege on remote computers. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

Common reasons for failure include an invalid computer name, an inaccessible computer, or insufficient privilege.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/928c2d48-daa5-4c27-816b-766adedba7eb">Displaying the Shutdown Dialog Box</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cad54fea-7f59-438c-83ac-f0160d81496b">InitiateSystemShutdown</a>



<a href="https://msdn.microsoft.com/acadf58f-3f68-4fa1-bdcf-8f85c8479263">Shutting Down</a>



<a href="https://msdn.microsoft.com/6a08a769-1acf-49eb-ba95-beaf56a374bf">System Shutdown
    Functions</a>
 

 

