---
UID: NN:workspaceruntime.IWorkspaceReportMessage
title: IWorkspaceReportMessage (workspaceruntime.h)
description: Exposes methods that support error message handling for remote workspaces.helpviewer_keywords: ["IWorkspaceReportMessage","IWorkspaceReportMessage interface [Remote Desktop Services]","IWorkspaceReportMessage interface [Remote Desktop Services]","described","termserv.iworkspacereportmessage","workspaceruntime/IWorkspaceReportMessage"]
old-location: termserv\iworkspacereportmessage.htm
tech.root: TermServ
ms.assetid: 841fce89-2996-42eb-81fc-7d6f8f864398
ms.date: 12/05/2018
ms.keywords: IWorkspaceReportMessage, IWorkspaceReportMessage interface [Remote Desktop Services], IWorkspaceReportMessage interface [Remote Desktop Services],described, termserv.iworkspacereportmessage, workspaceruntime/IWorkspaceReportMessage
f1_keywords:
- workspaceruntime/IWorkspaceReportMessage
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WkspRt.exe
api_name:
- IWorkspaceReportMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspaceReportMessage interface


## -description


Exposes methods that support error message handling for remote workspaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceReportMessage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWorkspaceReportMessage</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacereportmessage-iserrormessageregistered">IsErrorMessageRegistered</a>
</td>
<td align="left" width="63%">
Determines whether a specified error message is registered in a specified workspace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacereportmessage-registererrorevent">RegisterErrorEvent</a>
</td>
<td align="left" width="63%">
Registers the specified error event message to use in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacereportmessage-registererrorlogmessage">RegisterErrorLogMessage</a>
</td>
<td align="left" width="63%">
Registers the specified error log message to use in the UI.

</td>
</tr>
</table> 

