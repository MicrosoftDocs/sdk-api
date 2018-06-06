---
UID: NF:winuser.ExitWindowsEx
title: ExitWindowsEx function
author: windows-sdk-content
description: Logs off the interactive user, shuts down the system, or shuts down and restarts the system.
old-location: base\exitwindowsex.htm
old-project: Shutdown
ms.assetid: f44ccb66-10bd-4ee6-93e1-16948cf10e50
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EWX_FORCE, EWX_FORCEIFHUNG, EWX_HYBRID_SHUTDOWN, EWX_LOGOFF, EWX_POWEROFF, EWX_REBOOT, EWX_RESTARTAPPS, EWX_SHUTDOWN, ExitWindowsEx, ExitWindowsEx function, _win32_exitwindowsex, base.exitwindowsex, winuser/ExitWindowsEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ExitWindowsEx
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ExitWindowsEx function


## -description


Logs off the interactive user, shuts down the system, or shuts down and restarts the system. It sends the 
<a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message to all applications to determine if they can be terminated.


## -parameters




### -param uFlags [in]

The shutdown type. This parameter must include one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EWX_HYBRID_SHUTDOWN"></a><a id="ewx_hybrid_shutdown"></a><dl>
<dt><b>EWX_HYBRID_SHUTDOWN</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
<b>Beginning with Windows 8:  </b>You can prepare the system for a faster startup by combining the <b>EWX_HYBRID_SHUTDOWN</b> flag with the <b>EWX_SHUTDOWN</b> flag. 

</td>
</tr>
<tr>
<td width="40%"><a id="EWX_LOGOFF"></a><a id="ewx_logoff"></a><dl>
<dt><b>EWX_LOGOFF</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Shuts down all processes running in the logon session of the process that called the 
<b>ExitWindowsEx</b> function. Then it logs the user off.

This flag can be used only by processes running in an interactive user's logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="EWX_POWEROFF"></a><a id="ewx_poweroff"></a><dl>
<dt><b>EWX_POWEROFF</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Shuts down the system and turns off the power. The system must support the power-off feature. 




The calling process must have the SE_SHUTDOWN_NAME privilege. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="EWX_REBOOT"></a><a id="ewx_reboot"></a><dl>
<dt><b>EWX_REBOOT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Shuts down the system and then restarts the system. 




The calling process must have the SE_SHUTDOWN_NAME privilege. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="EWX_RESTARTAPPS"></a><a id="ewx_restartapps"></a><dl>
<dt><b>EWX_RESTARTAPPS</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Shuts down the system and then restarts it, as well as any applications that have been registered for restart using the <a href="https://msdn.microsoft.com/f4cd25b3-2aee-460f-9f9f-b45ecded094f">RegisterApplicationRestart</a> function. These application receive the <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message with <i>lParam</i> set to the ENDSESSION_CLOSEAPP value. For more information, see <a href="https://msdn.microsoft.com/97b1df63-65a9-47b4-891b-e4a754882b89">Guidelines for Applications</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="EWX_SHUTDOWN"></a><a id="ewx_shutdown"></a><dl>
<dt><b>EWX_SHUTDOWN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Shuts down the system to a point at which it is safe to turn off the power. All file buffers have been flushed to disk, and all running processes have stopped. 

The calling process must have the SE_SHUTDOWN_NAME privilege. For more information, see the following Remarks section.

Specifying this flag will not turn off the power even if the system supports the power-off feature. You must specify EWX_POWEROFF to do this.<b>Windows XP with SP1:  </b>If the system supports the power-off feature, specifying this flag turns off the power.



</td>
</tr>
</table>
 

This parameter can optionally include one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EWX_FORCE"></a><a id="ewx_force"></a><dl>
<dt><b>EWX_FORCE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This flag has no effect if terminal services is enabled. Otherwise, the system does not send the 
<a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message. This can cause applications to lose data. Therefore, you should only use this flag in an emergency.

</td>
</tr>
<tr>
<td width="40%"><a id="EWX_FORCEIFHUNG"></a><a id="ewx_forceifhung"></a><dl>
<dt><b>EWX_FORCEIFHUNG</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Forces processes to terminate if they do not respond to the 
<a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> or 
<a href="https://msdn.microsoft.com/9bf04f24-da1e-4680-a47b-28e9c500635e">WM_ENDSESSION</a> message within the timeout interval. For more information, see the Remarks.

</td>
</tr>
</table>
 


### -param dwReason [in]

The reason for initiating the shutdown. This parameter must be one of the 
<a href="https://msdn.microsoft.com/db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf">system shutdown reason codes</a>.

If this parameter is zero, the SHTDN_REASON_FLAG_PLANNED reason code  will not be set and therefore the default action is an undefined shutdown that is logged as "No title for this reason could be found". By default, it is also an unplanned shutdown. Depending on how the system is configured, an unplanned shutdown triggers the creation of a file that contains the system state information, which can delay shutdown. Therefore, do not use zero for this parameter.


## -returns



If the function succeeds, the return value is nonzero. Because the function executes asynchronously, a nonzero return value indicates that the shutdown has been initiated. It does not indicate whether the shutdown will succeed. It is possible that the system, the user, or another application will abort the shutdown.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>ExitWindowsEx</b> function returns as soon as it has initiated the shutdown process. The shutdown or logoff then proceeds asynchronously. The function is designed to stop all processes in the caller's logon session. Therefore, if you are not the interactive user, the function can succeed without actually shutting down the computer. If you are not the interactive user, use the 
<a href="https://msdn.microsoft.com/cad54fea-7f59-438c-83ac-f0160d81496b">InitiateSystemShutdown</a> or 
<a href="https://msdn.microsoft.com/4536cf76-7669-42b1-8c44-9f5e368424cc">InitiateSystemShutdownEx</a> function.

A non-zero return value does not mean the logoff was or will be successful. The shutdown is an asynchronous process, and it can occur long  after the API call has returned, or not  at all. Even if the timeout value is zero,  the shutdown can still be aborted by applications, services, or even the system. The non-zero return value indicates that the validation of the rights and parameters was  successful and that the system accepted the shutdown request.

When this function is called, the caller must specify whether or not applications with unsaved changes should be forcibly closed.  If the caller chooses not to force these applications to close and an application with unsaved changes is running on the console session, the shutdown will remain in progress until the user logged into the console session aborts the shutdown, saves changes, closes the application, or forces the application to close.  During this period, the shutdown may not be aborted except by the console user, and another shutdown may not be initiated.

Calling this function with the value of the <i>uFlags</i> parameter set to EWX_FORCE avoids this situation. Remember that doing this  may result in loss of data.

To set a shutdown priority for an application relative to other applications in the system, use the 
<a href="https://msdn.microsoft.com/c467950e-31e1-4608-a08a-0736a5524e0e">SetProcessShutdownParameters</a> function.

During a shutdown or log-off operation, running applications are allowed a specific amount of time to respond to the shutdown request. If this time expires before all applications have stopped, the system displays a user interface that allows the user to forcibly shut down the system or to cancel the shutdown request. If the EWX_FORCE value is specified, the system forces running applications to stop when the time expires.

If the EWX_FORCEIFHUNG value is specified, the system forces hung applications to close and does not display the dialog box.

Console processes receive a separate notification message, CTRL_SHUTDOWN_EVENT or CTRL_LOGOFF_EVENT, as the situation warrants. A console process routes these messages to its 
<a href="base.handlerroutine">HandlerRoutine</a> function. 
<b>ExitWindowsEx</b> sends these notification messages asynchronously; thus, an application cannot assume that the console notification messages have been handled when a call to 
<b>ExitWindowsEx</b> returns.

To shut down or restart the system, the calling process must use the 
<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function to enable the SE_SHUTDOWN_NAME privilege. For more information, see 
<a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/bf8723aa-1c7f-4761-9034-d5a9447a4bc4">How to Shut Down the System</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="base.handlerroutine">HandlerRoutine</a>



<a href="https://msdn.microsoft.com/906d92f1-7cbe-454e-9c71-34b4383aebab">Logging Off</a>



<a href="https://msdn.microsoft.com/c467950e-31e1-4608-a08a-0736a5524e0e">SetProcessShutdownParameters</a>



<a href="https://msdn.microsoft.com/acadf58f-3f68-4fa1-bdcf-8f85c8479263">Shutting Down</a>



<a href="https://msdn.microsoft.com/6a08a769-1acf-49eb-ba95-beaf56a374bf">System Shutdown
		  Functions</a>
 

 

