---
UID: NF:workspaceruntime.IWorkspace2.StartRemoteApplicationEx
title: IWorkspace2::StartRemoteApplicationEx
author: windows-sdk-content
description: Not supported.
old-location: termserv\iworkspace2_startremoteapplicationex.htm
old-project: TermServ
ms.assetid: df901da6-6464-4ed3-abbb-16756f90ccf1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWorkspace2 interface [Remote Desktop Services],StartRemoteApplicationEx method, IWorkspace2.StartRemoteApplicationEx, IWorkspace2::StartRemoteApplicationEx, IWorkspace3 interface [Remote Desktop Services],StartRemoteApplicationEx method, IWorkspace3::StartRemoteApplicationEx, StartRemoteApplicationEx, StartRemoteApplicationEx method [Remote Desktop Services], StartRemoteApplicationEx method [Remote Desktop Services],IWorkspace2 interface, StartRemoteApplicationEx method [Remote Desktop Services],IWorkspace3 interface, StartRemoteApplicationEx method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],StartRemoteApplicationEx method, termserv.iworkspace2_startremoteapplicationex, workspaceruntime/IWorkspace2::StartRemoteApplicationEx, workspaceruntime/IWorkspace3::StartRemoteApplicationEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>StartRemoteApplicationEx</b> contains a number of new features: launching a 3rd party application when the remote destop first starts, handling multiple remote desktops, and launching with the web-based client UI.




## -see-also




<a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>



<a href="https://msdn.microsoft.com/a63240fb-8724-4cd2-b845-f48075f4cb57">IWorkspace3</a>
 

 

