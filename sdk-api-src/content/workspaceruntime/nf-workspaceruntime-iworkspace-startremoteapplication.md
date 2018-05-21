---
UID: NF:workspaceruntime.IWorkspace.StartRemoteApplication
title: IWorkspace::StartRemoteApplication
author: windows-driver-content
description: Starts a RemoteApp program.
old-location: termserv\iworkspace_startremoteapplication.htm
old-project: TermServ
ms.assetid: a1d7e0c2-90bc-49c9-b7d5-380e13af4bba
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IWorkspace interface [Remote Desktop Services],StartRemoteApplication method, IWorkspace.StartRemoteApplication, IWorkspace2 interface [Remote Desktop Services],StartRemoteApplication method, IWorkspace2::StartRemoteApplication, IWorkspace3 interface [Remote Desktop Services],StartRemoteApplication method, IWorkspace3::StartRemoteApplication, IWorkspace::StartRemoteApplication, StartRemoteApplication, StartRemoteApplication method [Remote Desktop Services], StartRemoteApplication method [Remote Desktop Services],IWorkspace interface, StartRemoteApplication method [Remote Desktop Services],IWorkspace2 interface, StartRemoteApplication method [Remote Desktop Services],IWorkspace3 interface, StartRemoteApplication method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],StartRemoteApplication method, termserv.iworkspace_startremoteapplication, workspaceruntime/IWorkspace2::StartRemoteApplication, workspaceruntime/IWorkspace3::StartRemoteApplication, workspaceruntime/IWorkspace::StartRemoteApplication
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
-	IWorkspace.StartRemoteApplication
-	IWorkspace2.StartRemoteApplication
-	IWorkspace3.StartRemoteApplication
-	Workspace.StartRemoteApplication
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspace::StartRemoteApplication


## -description


Starts a RemoteApp program.


## -parameters




### -param bstrWorkspaceId [in]

A string that contains the ID of the connection  in which to the start the application.


### -param psaParams [in]

A pointer to an array of <b>BSTR</b> values that contains  parameters to pass to the workspace runtime.

For RDP connections, this parameter contains two strings:

<ul>
<li>Serialized RDP file</li>
<li>Command line parameters for Remote Desktop Connection client</li>
</ul>

## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling the <b>StartRemoteApplication</b> method can result in a new connection.

When a custom client calls the <b>StartRemoteApplication</b> method, the workspace runtime verifies that the RDP file is properly signed. If the RDP file signature is not valid, the  user is prompted for new credentials with which to validate the file.




## -see-also




<a href="https://msdn.microsoft.com/7a94ef42-8a63-4709-816d-1f51a948d486">IWorkspace</a>



<a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>



<a href="https://msdn.microsoft.com/a63240fb-8724-4cd2-b845-f48075f4cb57">IWorkspace3</a>
 

 

