---
UID: NF:workspaceruntime.IWorkspaceReportMessage.RegisterErrorLogMessage
title: IWorkspaceReportMessage::RegisterErrorLogMessage
author: windows-driver-content
description: Registers the specified error message to use in the UI.
old-location: termserv\iworkspacereportmessage_registererrorlogmessage.htm
old-project: TermServ
ms.assetid: 3aca491f-2cbd-4f04-a06c-986c37e6ce5a
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IWorkspaceReportMessage interface [Remote Desktop Services],RegisterErrorLogMessage method, IWorkspaceReportMessage.RegisterErrorLogMessage, IWorkspaceReportMessage::RegisterErrorLogMessage, RegisterErrorLogMessage, RegisterErrorLogMessage method [Remote Desktop Services], RegisterErrorLogMessage method [Remote Desktop Services],IWorkspaceReportMessage interface, RegisterErrorLogMessage method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],RegisterErrorLogMessage method, termserv.iworkspacereportmessage_registererrorlogmessage, workspaceruntime/IWorkspaceReportMessage::RegisterErrorLogMessage
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
-	IWorkspaceReportMessage.RegisterErrorLogMessage
-	Workspace.RegisterErrorLogMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceReportMessage::RegisterErrorLogMessage


## -description


Registers the specified error message to use in the UI.


## -parameters




### -param bstrMessage [in]

A string containing the error message to use in the UI.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/841fce89-2996-42eb-81fc-7d6f8f864398">IWorkspaceReportMessage</a>
 

 

