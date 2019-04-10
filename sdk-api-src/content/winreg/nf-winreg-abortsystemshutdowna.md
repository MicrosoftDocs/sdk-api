---
UID: NF:winreg.AbortSystemShutdownA
title: AbortSystemShutdownA function (winreg.h)
author: windows-sdk-content
description: Stops a system shutdown that has been initiated.
old-location: base\abortsystemshutdown.htm
tech.root: Shutdown
ms.assetid: 41212640-6a06-4d2f-9b0e-5b2d77d561b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AbortSystemShutdown, AbortSystemShutdown function, AbortSystemShutdownA, AbortSystemShutdownW, _win32_abortsystemshutdown, base.abortsystemshutdown, winreg/AbortSystemShutdown, winreg/AbortSystemShutdownA, winreg/AbortSystemShutdownW
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AbortSystemShutdownW (Unicode) and AbortSystemShutdownA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-shutdown-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-shutdown-l1-1-1.dll
 - API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
 - Ext-MS-Win-AdvAPI32-shutdown-l1-1-0.dll
 - API-MS-Win-Core-Shutdown-Ansi-L1-1-0.dll
api_name:
 - AbortSystemShutdown
 - AbortSystemShutdownA
 - AbortSystemShutdownW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AbortSystemShutdownA function


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
 

 

