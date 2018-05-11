---
UID: NF:workspaceruntime.IWorkspaceScriptable2.ResourceDismissed
title: IWorkspaceScriptable2::ResourceDismissed
author: windows-driver-content
description: Alerts the user that a resource has been disabled or otherwise dismissed.
old-location: termserv\iworkspacescriptable2_resourcedismissed.htm
old-project: TermServ
ms.assetid: e45d806c-56de-4f76-a76a-ba6db63f4ac2
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IWorkspaceScriptable2 interface [Remote Desktop Services],ResourceDismissed method, IWorkspaceScriptable2.ResourceDismissed, IWorkspaceScriptable2::ResourceDismissed, IWorkspaceScriptable3 interface [Remote Desktop Services],ResourceDismissed method, IWorkspaceScriptable3::ResourceDismissed, ResourceDismissed, ResourceDismissed method [Remote Desktop Services], ResourceDismissed method [Remote Desktop Services],IWorkspaceScriptable2 interface, ResourceDismissed method [Remote Desktop Services],IWorkspaceScriptable3 interface, ResourceDismissed method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],ResourceDismissed method, termserv.iworkspacescriptable2_resourcedismissed, workspaceruntime/IWorkspaceScriptable2::ResourceDismissed, workspaceruntime/IWorkspaceScriptable3::ResourceDismissed
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
-	IWorkspaceScriptable2.ResourceDismissed
-	IWorkspaceScriptable3.ResourceDismissed
-	Workspace.ResourceDismissed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceScriptable2::ResourceDismissed


## -description


Alerts the user that a resource has been disabled or otherwise dismissed.


## -parameters




### -param bstrWorkspaceId [in]

String containing the ID of the workspace that contains the unavailable resource.


### -param bstrWorkspaceFriendlyName [in]

String containing the friendly name of the workspace that holds the unavailable resource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>



<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

