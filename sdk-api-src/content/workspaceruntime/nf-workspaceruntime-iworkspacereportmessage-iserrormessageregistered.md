---
UID: NF:workspaceruntime.IWorkspaceReportMessage.IsErrorMessageRegistered
title: IWorkspaceReportMessage::IsErrorMessageRegistered (workspaceruntime.h)
description: Determines whether a specified error message is registered in a specified workspace.
helpviewer_keywords: ["IWorkspaceReportMessage interface [Remote Desktop Services]","IsErrorMessageRegistered method","IWorkspaceReportMessage.IsErrorMessageRegistered","IWorkspaceReportMessage::IsErrorMessageRegistered","IsErrorMessageRegistered","IsErrorMessageRegistered method [Remote Desktop Services]","IsErrorMessageRegistered method [Remote Desktop Services]","IWorkspaceReportMessage interface","IsErrorMessageRegistered method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","IsErrorMessageRegistered method","termserv.iworkspacereportmessage_iserrormessageregistered","workspaceruntime/IWorkspaceReportMessage::IsErrorMessageRegistered"]
old-location: termserv\iworkspacereportmessage_iserrormessageregistered.htm
tech.root: TermServ
ms.assetid: ea66553b-915b-4244-add7-08c7bc255203
ms.date: 12/05/2018
ms.keywords: IWorkspaceReportMessage interface [Remote Desktop Services],IsErrorMessageRegistered method, IWorkspaceReportMessage.IsErrorMessageRegistered, IWorkspaceReportMessage::IsErrorMessageRegistered, IsErrorMessageRegistered, IsErrorMessageRegistered method [Remote Desktop Services], IsErrorMessageRegistered method [Remote Desktop Services],IWorkspaceReportMessage interface, IsErrorMessageRegistered method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],IsErrorMessageRegistered method, termserv.iworkspacereportmessage_iserrormessageregistered, workspaceruntime/IWorkspaceReportMessage::IsErrorMessageRegistered
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
 - IWorkspaceReportMessage::IsErrorMessageRegistered
 - workspaceruntime/IWorkspaceReportMessage::IsErrorMessageRegistered
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
 - IWorkspaceReportMessage.IsErrorMessageRegistered
 - Workspace.IsErrorMessageRegistered
---

# IWorkspaceReportMessage::IsErrorMessageRegistered


## -description

Determines whether a specified error message is registered in a specified workspace.

## -parameters

### -param bstrWkspId [in]

A string containing the ID of the workspace to check.

### -param dwErrorType [in]

The error type associated with the error message.

### -param bstrErrorMessageType [in]

A string containing the error message type.

### -param dwErrorCode [in]

The error code of the event.

### -param pfErrorExist [out, retval]

On success, returns a pointer to <b>VARIANT_TRUE</b> if the error message is registered in the specified workspace; otherwise, <b>VARIANT_FALSE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage">IWorkspaceReportMessage</a>