---
UID: NF:workspaceruntime.IWorkspaceReportMessage.RegisterErrorLogMessage
title: IWorkspaceReportMessage::RegisterErrorLogMessage (workspaceruntime.h)
description: Registers the specified error message to use in the UI.
helpviewer_keywords: ["IWorkspaceReportMessage interface [Remote Desktop Services]","RegisterErrorLogMessage method","IWorkspaceReportMessage.RegisterErrorLogMessage","IWorkspaceReportMessage::RegisterErrorLogMessage","RegisterErrorLogMessage","RegisterErrorLogMessage method [Remote Desktop Services]","RegisterErrorLogMessage method [Remote Desktop Services]","IWorkspaceReportMessage interface","RegisterErrorLogMessage method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","RegisterErrorLogMessage method","termserv.iworkspacereportmessage_registererrorlogmessage","workspaceruntime/IWorkspaceReportMessage::RegisterErrorLogMessage"]
old-location: termserv\iworkspacereportmessage_registererrorlogmessage.htm
tech.root: TermServ
ms.assetid: 3aca491f-2cbd-4f04-a06c-986c37e6ce5a
ms.date: 12/05/2018
ms.keywords: IWorkspaceReportMessage interface [Remote Desktop Services],RegisterErrorLogMessage method, IWorkspaceReportMessage.RegisterErrorLogMessage, IWorkspaceReportMessage::RegisterErrorLogMessage, RegisterErrorLogMessage, RegisterErrorLogMessage method [Remote Desktop Services], RegisterErrorLogMessage method [Remote Desktop Services],IWorkspaceReportMessage interface, RegisterErrorLogMessage method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],RegisterErrorLogMessage method, termserv.iworkspacereportmessage_registererrorlogmessage, workspaceruntime/IWorkspaceReportMessage::RegisterErrorLogMessage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceReportMessage::RegisterErrorLogMessage
 - workspaceruntime/IWorkspaceReportMessage::RegisterErrorLogMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WkspRt.exe
api_name:
 - IWorkspaceReportMessage.RegisterErrorLogMessage
 - Workspace.RegisterErrorLogMessage
---

# IWorkspaceReportMessage::RegisterErrorLogMessage


## -description

Registers the specified error message to use in the UI.

## -parameters

### -param bstrMessage [in]

A string containing the error message to use in the UI.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage">IWorkspaceReportMessage</a>