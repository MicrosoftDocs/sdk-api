---
UID: NF:workspaceruntime.IWorkspace2.StartRemoteApplicationEx
title: IWorkspace2::StartRemoteApplicationEx (workspaceruntime.h)
description: Not supported. (IWorkspace2.StartRemoteApplicationEx)
helpviewer_keywords: ["IWorkspace2 interface [Remote Desktop Services]","StartRemoteApplicationEx method","IWorkspace2.StartRemoteApplicationEx","IWorkspace2::StartRemoteApplicationEx","IWorkspace3 interface [Remote Desktop Services]","StartRemoteApplicationEx method","IWorkspace3::StartRemoteApplicationEx","StartRemoteApplicationEx","StartRemoteApplicationEx method [Remote Desktop Services]","StartRemoteApplicationEx method [Remote Desktop Services]","IWorkspace2 interface","StartRemoteApplicationEx method [Remote Desktop Services]","IWorkspace3 interface","StartRemoteApplicationEx method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","StartRemoteApplicationEx method","termserv.iworkspace2_startremoteapplicationex","workspaceruntime/IWorkspace2::StartRemoteApplicationEx","workspaceruntime/IWorkspace3::StartRemoteApplicationEx"]
old-location: termserv\iworkspace2_startremoteapplicationex.htm
tech.root: TermServ
ms.assetid: df901da6-6464-4ed3-abbb-16756f90ccf1
ms.date: 12/05/2018
ms.keywords: IWorkspace2 interface [Remote Desktop Services],StartRemoteApplicationEx method, IWorkspace2.StartRemoteApplicationEx, IWorkspace2::StartRemoteApplicationEx, IWorkspace3 interface [Remote Desktop Services],StartRemoteApplicationEx method, IWorkspace3::StartRemoteApplicationEx, StartRemoteApplicationEx, StartRemoteApplicationEx method [Remote Desktop Services], StartRemoteApplicationEx method [Remote Desktop Services],IWorkspace2 interface, StartRemoteApplicationEx method [Remote Desktop Services],IWorkspace3 interface, StartRemoteApplicationEx method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],StartRemoteApplicationEx method, termserv.iworkspace2_startremoteapplicationex, workspaceruntime/IWorkspace2::StartRemoteApplicationEx, workspaceruntime/IWorkspace3::StartRemoteApplicationEx
req.header: workspaceruntime.h
req.include-header: Workspaceruntime.h
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
 - IWorkspace2::StartRemoteApplicationEx
 - workspaceruntime/IWorkspace2::StartRemoteApplicationEx
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
 - IWorkspace2.StartRemoteApplicationEx
 - IWorkspace3.StartRemoteApplicationEx
 - Workspace.StartRemoteApplicationEx
---

# IWorkspace2::StartRemoteApplicationEx


## -description

Not supported.

Starts a RemoteApp program with additional options and features.

## -parameters

### -param bstrWorkspaceId [in]

A string that contains the ID of the connection  in which to the start the application.

### -param bstrRequestingAppId [in]

A string that contains the ID of an application to launch on the remote desktop.

### -param bstrRequestingAppFamilyName [in]

A string that contains the family name of the application to launch.

### -param bLaunchIntoImmersiveClient [in]

<b>VARIANT_TRUE</b> to make the remote application launch as though it were accessed via the web client, using the modern Remote Desktop protocol. <b>VARIANT_FALSE</b> to make the remote application launch using classic Terminal Server methodology.

### -param bstrImmersiveClientActivationContext [in]

A string containing the context for the specific remote desktop client.

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

<b>StartRemoteApplicationEx</b> contains a number of new features: launching a 3rd party application when the remote desktop first starts, handling multiple remote desktops, and launching with the web-based client UI.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2">IWorkspace2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3">IWorkspace3</a>
