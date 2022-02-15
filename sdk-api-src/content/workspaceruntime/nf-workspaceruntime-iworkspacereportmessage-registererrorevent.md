---
UID: NF:workspaceruntime.IWorkspaceReportMessage.RegisterErrorEvent
title: IWorkspaceReportMessage::RegisterErrorEvent (workspaceruntime.h)
description: Registers the specified error event message to use in the UI.
helpviewer_keywords: ["IWorkspaceReportMessage interface [Remote Desktop Services]","RegisterErrorEvent method","IWorkspaceReportMessage.RegisterErrorEvent","IWorkspaceReportMessage::RegisterErrorEvent","RegisterErrorEvent","RegisterErrorEvent method [Remote Desktop Services]","RegisterErrorEvent method [Remote Desktop Services]","IWorkspaceReportMessage interface","RegisterErrorEvent method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","RegisterErrorEvent method","termserv.iworkspacereportmessage_registererrorevent","workspaceruntime/IWorkspaceReportMessage::RegisterErrorEvent"]
old-location: termserv\iworkspacereportmessage_registererrorevent.htm
tech.root: TermServ
ms.assetid: d8c85912-7766-4d1c-8004-d9104a4dbc09
ms.date: 12/05/2018
ms.keywords: IWorkspaceReportMessage interface [Remote Desktop Services],RegisterErrorEvent method, IWorkspaceReportMessage.RegisterErrorEvent, IWorkspaceReportMessage::RegisterErrorEvent, RegisterErrorEvent, RegisterErrorEvent method [Remote Desktop Services], RegisterErrorEvent method [Remote Desktop Services],IWorkspaceReportMessage interface, RegisterErrorEvent method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],RegisterErrorEvent method, termserv.iworkspacereportmessage_registererrorevent, workspaceruntime/IWorkspaceReportMessage::RegisterErrorEvent
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
 - IWorkspaceReportMessage::RegisterErrorEvent
 - workspaceruntime/IWorkspaceReportMessage::RegisterErrorEvent
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
 - IWorkspaceReportMessage.RegisterErrorEvent
 - Workspace.RegisterErrorEvent
---

# IWorkspaceReportMessage::RegisterErrorEvent


## -description

Registers the specified error event message to use in the UI.

## -parameters

### -param bstrWkspId [in]

A string containing the workspace ID in which the error event is to be registered.

### -param dwErrorType [in]

The error type of the event.

### -param bstrErrorMessageType [in]

A string containing the error message.

### -param dwErrorCode [in]

The error code for the event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage">IWorkspaceReportMessage</a>