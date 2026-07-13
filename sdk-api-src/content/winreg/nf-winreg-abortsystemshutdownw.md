---
UID: NF:winreg.AbortSystemShutdownW
title: AbortSystemShutdownW function (winreg.h)
description: Stops a system shutdown that has been initiated. (Unicode)
helpviewer_keywords: ["AbortSystemShutdown", "AbortSystemShutdown function", "AbortSystemShutdownW", "_win32_abortsystemshutdown", "base.abortsystemshutdown", "winreg/AbortSystemShutdown", "winreg/AbortSystemShutdownW"]
old-location: base\abortsystemshutdown.htm
tech.root: base
ms.assetid: 41212640-6a06-4d2f-9b0e-5b2d77d561b0
ms.date: 12/05/2018
ms.keywords: AbortSystemShutdown, AbortSystemShutdown function, AbortSystemShutdownA, AbortSystemShutdownW, _win32_abortsystemshutdown, base.abortsystemshutdown, winreg/AbortSystemShutdown, winreg/AbortSystemShutdownA, winreg/AbortSystemShutdownW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AbortSystemShutdownW
 - winreg/AbortSystemShutdownW
dev_langs:
 - c++
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<a href="/windows/desktop/api/winreg/nf-winreg-initiatesystemshutdowna">InitiateSystemShutdown</a> and 
<a href="/windows/desktop/api/winreg/nf-winreg-initiatesystemshutdownexa">InitiateSystemShutdownEx</a> functions display a dialog box that notifies the user that the system is shutting down. During the shutdown time-out period, the 
<b>AbortSystemShutdown</b> function can prevent the system from shutting down.

<b>Windows Server 2003 and Windows XP with SP1:  </b>If the computer to be shut down is a Terminal Services server, the system displays a dialog box to all local and remote users warning them that shutdown has been initiated. If shutdown is prevented by 
<b>AbortSystemShutdown</b>, the system displays dialog box to the users informing them that the server is no longer shutting down.

To stop the local computer from shutting down, the calling process must have the SE_SHUTDOWN_NAME privilege. To stop a remote computer from shutting down, the calling process must have the SE_REMOTE_SHUTDOWN_NAME privilege on the remote computer. By default, users can enable the SE_SHUTDOWN_NAME privilege on the computer they are logged onto, and administrators can enable the SE_REMOTE_SHUTDOWN_NAME privilege on remote computers. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Common reasons for failure include an invalid computer name, an inaccessible computer, or insufficient privilege.


#### Examples

For an example, see 
<a href="/windows/desktop/Shutdown/displaying-the-shutdown-dialog-box">Displaying the Shutdown Dialog Box</a>.

<div class="code"></div>




> [!NOTE]
> The winreg.h header defines AbortSystemShutdown as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-initiatesystemshutdowna">InitiateSystemShutdown</a>



<a href="/windows/desktop/Shutdown/shutting-down">Shutting Down</a>



<a href="/windows/desktop/Shutdown/system-shutdown-functions">System Shutdown
    Functions</a>
