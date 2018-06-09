---
UID: NN:shobjidl_core.IPackageDebugSettings
title: IPackageDebugSettings
author: windows-sdk-content
description: Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.
old-location: shell\IPackageDebugSettings.htm
old-project: shell
ms.assetid: e407c4ca-0de1-4b17-bb83-5c4128952d48
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Shell], IPackageDebugSettings interface [Windows Shell],described, shell.IPackageDebugSettings, shobjidl_core/IPackageDebugSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IPackageDebugSettings interface


## -description


Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPackageDebugSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPackageDebugSettings</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/30ef83f0-cad1-4aee-9b70-0fe7189aff9e">ActivateBackgroundTask</a>
</td>
<td align="left" width="63%">
Activates the specified background task. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/102e57be-296e-44ec-8211-f2c2d5eae1e6">DisableDebugging</a>
</td>
<td align="left" width="63%">
Disables debug mode for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3afae41-b46e-47c8-95bb-a0aa747c6353">EnableDebugging</a>
</td>
<td align="left" width="63%">
Enables debug mode for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14a516c8-fb15-41b6-807c-b14d81148e0e">EnumerateBackgroundTasks</a>
</td>
<td align="left" width="63%">
Gets the background tasks that are provided by the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39560adc-9d35-48ec-8b70-2ed4b83dd1f6">GetPackageExecutionState</a>
</td>
<td align="left" width="63%">
Returns the current execution state of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>
</td>
<td align="left" width="63%">
Register for package state-change notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f0b3188-4c58-4ff6-983e-912131a7c934">Resume</a>
</td>
<td align="left" width="63%">
Resumes the processes of the package if they are currently suspended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7794703-08ff-40a8-8807-a09e35a4bb8f">SetTargetSessionId</a>
</td>
<td align="left" width="63%">
Sets the session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f5331d-194f-4beb-9c59-f6899186b393">StartServicing</a>
</td>
<td align="left" width="63%">
Suspends and terminates the non-background portion of the apps associated with the specified package and cancels the background tasks associated with the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9f40c32-afbe-4f1f-9693-72a757d93a05">StartSessionRedirection</a>
</td>
<td align="left" width="63%">
Causes background tasks for the specified package to activate  in the specified user session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/129ea98a-e0c3-4472-918c-6d9aa4858c4b">StopServicing</a>
</td>
<td align="left" width="63%">
Completes the previous servicing operation that was started by a call to the  <a href="https://msdn.microsoft.com/40f5331d-194f-4beb-9c59-f6899186b393">StartServicing</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6edd4f9a-c9e8-45eb-a86b-a04116530aad">StopSessionRedirection</a>
</td>
<td align="left" width="63%">
Stops redirection of background tasks for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927278">Suspend</a>
</td>
<td align="left" width="63%">
Suspends the processes of the package if they are currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e49faeaa-8fd8-4233-94ac-0899177a9bb3">TerminateAllProcesses</a>
</td>
<td align="left" width="63%">
Terminates all processes for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CFCDA0AD-83D5-43DD-A7DD-C121563BF3DB">UnregisterForPackageStateChanges</a>
</td>
<td align="left" width="63%">
Stops receiving package state-change notifications associated with a previous call to <a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>.

</td>
</tr>
</table> 


## -remarks



Any debug options set remain in effect until they are cleared or this interface is released.

For debug settings to take effect on Internet Explorer in the new Windows UI, use "DefaultBrowser_NOPUBLISHERID" as the <i>packageFullName</i> parameter  for  <a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a> methods. 



