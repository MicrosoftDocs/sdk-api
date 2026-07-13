---
UID: NF:workspaceruntime.IWorkspace.StartRemoteApplication
title: IWorkspace::StartRemoteApplication (workspaceruntime.h)
description: Starts a RemoteApp program.
helpviewer_keywords: ["IWorkspace interface [Remote Desktop Services]","StartRemoteApplication method","IWorkspace.StartRemoteApplication","IWorkspace2 interface [Remote Desktop Services]","StartRemoteApplication method","IWorkspace2::StartRemoteApplication","IWorkspace3 interface [Remote Desktop Services]","StartRemoteApplication method","IWorkspace3::StartRemoteApplication","IWorkspace::StartRemoteApplication","StartRemoteApplication","StartRemoteApplication method [Remote Desktop Services]","StartRemoteApplication method [Remote Desktop Services]","IWorkspace interface","StartRemoteApplication method [Remote Desktop Services]","IWorkspace2 interface","StartRemoteApplication method [Remote Desktop Services]","IWorkspace3 interface","StartRemoteApplication method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","StartRemoteApplication method","termserv.iworkspace_startremoteapplication","workspaceruntime/IWorkspace2::StartRemoteApplication","workspaceruntime/IWorkspace3::StartRemoteApplication","workspaceruntime/IWorkspace::StartRemoteApplication"]
old-location: termserv\iworkspace_startremoteapplication.htm
tech.root: TermServ
ms.assetid: a1d7e0c2-90bc-49c9-b7d5-380e13af4bba
ms.date: 12/05/2018
ms.keywords: IWorkspace interface [Remote Desktop Services],StartRemoteApplication method, IWorkspace.StartRemoteApplication, IWorkspace2 interface [Remote Desktop Services],StartRemoteApplication method, IWorkspace2::StartRemoteApplication, IWorkspace3 interface [Remote Desktop Services],StartRemoteApplication method, IWorkspace3::StartRemoteApplication, IWorkspace::StartRemoteApplication, StartRemoteApplication, StartRemoteApplication method [Remote Desktop Services], StartRemoteApplication method [Remote Desktop Services],IWorkspace interface, StartRemoteApplication method [Remote Desktop Services],IWorkspace2 interface, StartRemoteApplication method [Remote Desktop Services],IWorkspace3 interface, StartRemoteApplication method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],StartRemoteApplication method, termserv.iworkspace_startremoteapplication, workspaceruntime/IWorkspace2::StartRemoteApplication, workspaceruntime/IWorkspace3::StartRemoteApplication, workspaceruntime/IWorkspace::StartRemoteApplication
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspace::StartRemoteApplication
 - workspaceruntime/IWorkspace::StartRemoteApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wksprt.exe
api_name:
 - IWorkspace.StartRemoteApplication
 - IWorkspace2.StartRemoteApplication
 - IWorkspace3.StartRemoteApplication
 - Workspace.StartRemoteApplication
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling the <b>StartRemoteApplication</b> method can result in a new connection.

When a custom client calls the <b>StartRemoteApplication</b> method, the workspace runtime verifies that the RDP file is properly signed. If the RDP file signature is not valid, the  user is prompted for new credentials with which to validate the file.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace">IWorkspace</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2">IWorkspace2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3">IWorkspace3</a>