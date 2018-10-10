---
UID: NN:shobjidl_core.IPackageDebugSettings
title: IPackageDebugSettings
author: windows-sdk-content
description: Enables debugger developers control over the lifecycle of a Windows Store app, such as when it is suspended or resumed.
old-location: winrt\ipackagedebugsettings.htm
tech.root: WinRT
ms.assetid: cae72152-c9d2-4791-b3f8-1187fb2a4d6c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], IPackageDebugSettings interface [Windows Runtime],described, shobjidl_core/IPackageDebugSettings, winrt.ipackagedebugsettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - shobjidl_core.h
api_name:
 - IPackageDebugSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings interface


## -description


Enables debugger developers control over the lifecycle of a Windows Store app, such as when it is suspended or resumed.


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
<a href="https://msdn.microsoft.com/5ACDAB41-5904-409B-86B2-96865B761868">ActivateBackgroundTask</a>
</td>
<td align="left" width="63%">
Activates the specified background task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad7efefb-aacd-48fa-bfe6-26271bd03b86">DisableDebugging</a>
</td>
<td align="left" width="63%">
Disables debug mode for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6219e8d7-0631-482f-b602-b0453d4b1e70">EnableDebugging</a>
</td>
<td align="left" width="63%">
Enables debug mode for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C86103F6-6893-483C-8237-CBBA71C784D2">EnumerateBackgroundTasks</a>
</td>
<td align="left" width="63%">
Enumerates background tasks for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D3FD95D-C958-4388-90F4-03DE2F75DF64">GetPackageExecutionState</a>
</td>
<td align="left" width="63%">
Gets the execution state for the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B53CF95C-FD40-45E2-869B-32F089986D13">RegisterForPackageStateChanges</a>
</td>
<td align="left" width="63%">
Registers for changes in the state of the processes of the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5376e00-b4b7-4a81-a84c-3a46758fe130">Resume</a>
</td>
<td align="left" width="63%">
Resumes the processes of the package if they are currently suspended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b262ac9-2e15-48d5-ad09-8b46234601e6">SetTargetSessionId</a>
</td>
<td align="left" width="63%">
Sets the session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8DBD9EF8-F350-4B92-BC4C-6E3ACBBF7D95">StartServicing</a>
</td>
<td align="left" width="63%">
Terminates the application and prevents new background task activations until a call to <a href="https://msdn.microsoft.com/91C20C41-8F20-4F9D-B22C-50D1D53FEB41">StopServicing</a> is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/686CF2EC-CEE7-4E6A-9E97-9DD80AE89131">StartSessionRedirection</a>
</td>
<td align="left" width="63%">
Starts redirection for the specified session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91C20C41-8F20-4F9D-B22C-50D1D53FEB41">StopServicing</a>
</td>
<td align="left" width="63%">
Stops servicing the processes of the package if they are currently being serviced.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2E0BB941-CD98-4DFE-A16D-93A6327AAA2B">StopSessionRedirection</a>
</td>
<td align="left" width="63%">
Stops redirection for the current session. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83f44285-46ed-4968-b0af-7964dfacf602">Suspend</a>
</td>
<td align="left" width="63%">
Suspends the processes of the package if they are currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54be6d31-c9b9-41c6-a90f-31f6b9caef70">TerminateAllProcesses</a>
</td>
<td align="left" width="63%">
Terminates all processes for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7EC7CCCB-1AE6-458C-A92C-4D303717EA15">UnregisterForPackageStateChanges</a>
</td>
<td align="left" width="63%">
Unregisters for changes in the state of the processes of the specified package.

</td>
</tr>
</table> 


## -remarks



Any debug options set remain in effect until they are cleared or this interface is released.

For debug settings to take effect on Internet Explorer in the new Windows UI, use "DefaultBrowser_NOPUBLISHERID" as the <i>packageFullName</i> parameter  for  <b>IPackageDebugSettings</b> methods. 



