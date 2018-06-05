---
UID: NF:workspaceruntime.IWorkspaceReportMessage.IsErrorMessageRegistered
title: IWorkspaceReportMessage::IsErrorMessageRegistered
author: windows-sdk-content
description: Determines whether a specified error message is registered in a specified workspace.
old-location: termserv\iworkspacereportmessage_iserrormessageregistered.htm
old-project: TermServ
ms.assetid: ea66553b-915b-4244-add7-08c7bc255203
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWorkspaceReportMessage interface [Remote Desktop Services],IsErrorMessageRegistered method, IWorkspaceReportMessage.IsErrorMessageRegistered, IWorkspaceReportMessage::IsErrorMessageRegistered, IsErrorMessageRegistered, IsErrorMessageRegistered method [Remote Desktop Services], IsErrorMessageRegistered method [Remote Desktop Services],IWorkspaceReportMessage interface, IsErrorMessageRegistered method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],IsErrorMessageRegistered method, termserv.iworkspacereportmessage_iserrormessageregistered, workspaceruntime/IWorkspaceReportMessage::IsErrorMessageRegistered
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WkspRt.exe
api_name:
-	IWorkspaceReportMessage.IsErrorMessageRegistered
-	Workspace.IsErrorMessageRegistered
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/841fce89-2996-42eb-81fc-7d6f8f864398">IWorkspaceReportMessage</a>
 

 

