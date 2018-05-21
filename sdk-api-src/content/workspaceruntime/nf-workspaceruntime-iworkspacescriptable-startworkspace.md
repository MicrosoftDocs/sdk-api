---
UID: NF:workspaceruntime.IWorkspaceScriptable.StartWorkspace
title: IWorkspaceScriptable::StartWorkspace
author: windows-driver-content
description: Associates user credentials and certificates with a connection ID.
old-location: termserv\iworkspacescriptable_startworkspace.htm
old-project: TermServ
ms.assetid: a2985ae1-7874-43e8-b0d3-ef3f13ac2f8d
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IWorkspaceScriptable interface [Remote Desktop Services],StartWorkspace method, IWorkspaceScriptable.StartWorkspace, IWorkspaceScriptable2 interface [Remote Desktop Services],StartWorkspace method, IWorkspaceScriptable2::StartWorkspace, IWorkspaceScriptable3 interface [Remote Desktop Services],StartWorkspace method, IWorkspaceScriptable3::StartWorkspace, IWorkspaceScriptable::StartWorkspace, StartWorkspace, StartWorkspace method [Remote Desktop Services], StartWorkspace method [Remote Desktop Services],IWorkspaceScriptable interface, StartWorkspace method [Remote Desktop Services],IWorkspaceScriptable2 interface, StartWorkspace method [Remote Desktop Services],IWorkspaceScriptable3 interface, StartWorkspace method [Remote Desktop Services],Workspace object, WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE, WKS_FLAG_CREDS_AUTHENTICATED, WKS_FLAG_PASSWORD_ENCRYPTED, Workspace object [Remote Desktop Services],StartWorkspace method, termserv.iworkspacescriptable_startworkspace, workspaceruntime/IWorkspaceScriptable2::StartWorkspace, workspaceruntime/IWorkspaceScriptable3::StartWorkspace, workspaceruntime/IWorkspaceScriptable::StartWorkspace
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
-	IWorkspaceScriptable.StartWorkspace
-	IWorkspaceScriptable2.StartWorkspace
-	IWorkspaceScriptable3.StartWorkspace
-	Workspace.StartWorkspace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceScriptable::StartWorkspace


## -description


Associates user credentials and certificates with a connection ID.


## -parameters




### -param bstrWorkspaceId [in]

A string that contains the connection ID.


### -param bstrUserName [in]

A string that contains a user name.


### -param bstrPassword [in]

A string that contains a password.


### -param bstrWorkspaceParams [in]

A string that contains one or more Secure Hash Algorithm 1 (SHA-1) hashes of signing certificates to associate with the specified connection ID. The hash values should be in hexadecimal string format and delimited by semicolons.


### -param lTimeout [in]

The time period, in minutes, after which the credentials are deleted.


### -param lFlags [in]

A flag that specifies  properties of the user credentials. This can be  a bitwise <b>OR</b> of the following values.



#### WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE (1 (0x1))

Delete credentials as soon as the last RemoteApp application is closed.



#### WKS_FLAG_PASSWORD_ENCRYPTED (2 (0x2))

The password is encrypted.



#### WKS_FLAG_CREDS_AUTHENTICATED (4 (0x4))

The user credentials are verified. If this flag is not set, you must call the <a href="https://msdn.microsoft.com/7b879234-07a2-43e7-83e8-c503e418f71e">OnAuthenticated</a> method before using the credentials.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.




## -see-also




<a href="https://msdn.microsoft.com/b6591369-d73f-4c7d-8525-428dffc9a341">IWorkspaceScriptable</a>



<a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>



<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

