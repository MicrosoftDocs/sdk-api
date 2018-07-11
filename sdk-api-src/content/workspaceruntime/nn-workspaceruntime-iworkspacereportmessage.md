---
UID: NN:workspaceruntime.IWorkspaceReportMessage
title: IWorkspaceReportMessage
author: windows-sdk-content
description: Exposes methods that support error message handling for remote workspaces.
old-location: termserv\iworkspacereportmessage.htm
old-project: TermServ
ms.assetid: 841fce89-2996-42eb-81fc-7d6f8f864398
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IWorkspaceReportMessage, IWorkspaceReportMessage interface [Remote Desktop Services], IWorkspaceReportMessage interface [Remote Desktop Services],described, termserv.iworkspacereportmessage, workspaceruntime/IWorkspaceReportMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: WkspRt.exe
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WkspRt.exe
api_name:
 - IWorkspaceReportMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceReportMessage interface


## -description


Exposes methods that support error message handling for remote workspaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceReportMessage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWorkspaceReportMessage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceReportMessage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea66553b-915b-4244-add7-08c7bc255203">IsErrorMessageRegistered</a>
</td>
<td align="left" width="63%">
Determines whether a specified error message is registered in a specified workspace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8c85912-7766-4d1c-8004-d9104a4dbc09">RegisterErrorEvent</a>
</td>
<td align="left" width="63%">
Registers the specified error event message to use in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3aca491f-2cbd-4f04-a06c-986c37e6ce5a">RegisterErrorLogMessage</a>
</td>
<td align="left" width="63%">
Registers the specified error log message to use in the UI.

</td>
</tr>
</table> 

