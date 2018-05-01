---
UID: NF:workspaceruntime.IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName
title: IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName method
author: windows-driver-content
description: Disconnects all existing connections associated with the connection that has the specified name.
old-location: termserv\iworkspacescriptable_disconnectworkspacebyfriendlyname.htm
old-project: TermServ
ms.assetid: e9cf9c1a-8400-4a69-9cf1-0dfa6fe6a38b
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: DisconnectWorkspaceByFriendlyName method [Remote Desktop Services], DisconnectWorkspaceByFriendlyName method [Remote Desktop Services], IWorkspaceScriptable interface, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services], IWorkspaceScriptable2 interface, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services], IWorkspaceScriptable3 interface, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services], Workspace object, DisconnectWorkspaceByFriendlyName,IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName, IWorkspaceScriptable, IWorkspaceScriptable interface [Remote Desktop Services], DisconnectWorkspaceByFriendlyName method, IWorkspaceScriptable2 interface [Remote Desktop Services], DisconnectWorkspaceByFriendlyName method, IWorkspaceScriptable2::DisconnectWorkspaceByFriendlyName, IWorkspaceScriptable3 interface [Remote Desktop Services], DisconnectWorkspaceByFriendlyName method, IWorkspaceScriptable3::DisconnectWorkspaceByFriendlyName, IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName, Workspace object [Remote Desktop Services], DisconnectWorkspaceByFriendlyName method, termserv.iworkspacescriptable_disconnectworkspacebyfriendlyname, workspaceruntime/IWorkspaceScriptable2::DisconnectWorkspaceByFriendlyName, workspaceruntime/IWorkspaceScriptable3::DisconnectWorkspaceByFriendlyName, workspaceruntime/IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wksprt.exe
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wksprt.exe
api_name:
-	IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName
-	IWorkspaceScriptable2.DisconnectWorkspaceByFriendlyName
-	IWorkspaceScriptable3.DisconnectWorkspaceByFriendlyName
-	Workspace.DisconnectWorkspaceByFriendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName method


## -description


Disconnects all existing connections associated with the connection that has the  specified name. It also deletes the corresponding entries from the RemoteApp and Desktop Connection store.


## -parameters




### -param bstrWorkspaceFriendlyName






#### - BSTR [in]

A string that contains the friendly name of the connection to disconnect.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b6591369-d73f-4c7d-8525-428dffc9a341">IWorkspaceScriptable</a>



<a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>



<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

