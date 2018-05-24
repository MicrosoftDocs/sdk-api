---
UID: NF:workspaceruntime.IWorkspaceReportMessage.RegisterErrorEvent
title: IWorkspaceReportMessage::RegisterErrorEvent
author: windows-driver-content
description: Registers the specified error event message to use in the UI.
old-location: termserv\iworkspacereportmessage_registererrorevent.htm
old-project: TermServ
ms.assetid: d8c85912-7766-4d1c-8004-d9104a4dbc09
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWorkspaceReportMessage interface [Remote Desktop Services],RegisterErrorEvent method, IWorkspaceReportMessage.RegisterErrorEvent, IWorkspaceReportMessage::RegisterErrorEvent, RegisterErrorEvent, RegisterErrorEvent method [Remote Desktop Services], RegisterErrorEvent method [Remote Desktop Services],IWorkspaceReportMessage interface, RegisterErrorEvent method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],RegisterErrorEvent method, termserv.iworkspacereportmessage_registererrorevent, workspaceruntime/IWorkspaceReportMessage::RegisterErrorEvent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WkspRt.exe
api_name:
-	IWorkspaceReportMessage.RegisterErrorEvent
-	Workspace.RegisterErrorEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/841fce89-2996-42eb-81fc-7d6f8f864398">IWorkspaceReportMessage</a>
 

 

