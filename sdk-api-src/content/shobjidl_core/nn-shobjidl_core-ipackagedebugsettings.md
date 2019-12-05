---
UID: NN:shobjidl_core.IPackageDebugSettings
title: IPackageDebugSettings (shobjidl_core.h)
description: Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.
old-location: shell\IPackageDebugSettings.htm
tech.root: shell
ms.assetid: e407c4ca-0de1-4b17-bb83-5c4128952d48
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Shell], IPackageDebugSettings interface [Windows Shell],described, shell.IPackageDebugSettings, shobjidl_core/IPackageDebugSettings
ms.topic: interface
f1_keywords:
- shobjidl_core/IPackageDebugSettings
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl_core.h
api_name:
- IPackageDebugSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPackageDebugSettings interface


## -description


Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPackageDebugSettings</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPackageDebugSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPackageDebugSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-activatebackgroundtask">ActivateBackgroundTask</a>
</td>
<td align="left" width="63%">
Activates the specified background task. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-disabledebugging">DisableDebugging</a>
</td>
<td align="left" width="63%">
Disables debug mode for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-enabledebugging">EnableDebugging</a>
</td>
<td align="left" width="63%">
Enables debug mode for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-enumeratebackgroundtasks">EnumerateBackgroundTasks</a>
</td>
<td align="left" width="63%">
Gets the background tasks that are provided by the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-getpackageexecutionstate">GetPackageExecutionState</a>
</td>
<td align="left" width="63%">
Returns the current execution state of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a>
</td>
<td align="left" width="63%">
Register for package state-change notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-resume">Resume</a>
</td>
<td align="left" width="63%">
Resumes the processes of the package if they are currently suspended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-settargetsessionid">SetTargetSessionId</a>
</td>
<td align="left" width="63%">
Sets the session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-startservicing">StartServicing</a>
</td>
<td align="left" width="63%">
Suspends and terminates the non-background portion of the apps associated with the specified package and cancels the background tasks associated with the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-startsessionredirection">StartSessionRedirection</a>
</td>
<td align="left" width="63%">
Causes background tasks for the specified package to activate  in the specified user session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-stopservicing">StopServicing</a>
</td>
<td align="left" width="63%">
Completes the previous servicing operation that was started by a call to the  <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-startservicing">StartServicing</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-stopsessionredirection">StopSessionRedirection</a>
</td>
<td align="left" width="63%">
Stops redirection of background tasks for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-suspend">Suspend</a>
</td>
<td align="left" width="63%">
Suspends the processes of the package if they are currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-terminateallprocesses">TerminateAllProcesses</a>
</td>
<td align="left" width="63%">
Terminates all processes for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-unregisterforpackagestatechanges">UnregisterForPackageStateChanges</a>
</td>
<td align="left" width="63%">
Stops receiving package state-change notifications associated with a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a>.

</td>
</tr>
</table> 


## -remarks



Any debug options set remain in effect until they are cleared or this interface is released.

For debug settings to take effect on Internet Explorer in the new Windows UI, use "DefaultBrowser_NOPUBLISHERID" as the <i>packageFullName</i> parameter  for  <a href="https://docs.microsoft.com/previous-versions/hh438393(v=vs.85)">IPackageDebugSettings</a> methods. 



