---
UID: NF:workspaceruntime.IWorkspaceScriptable.StartWorkspace
title: IWorkspaceScriptable::StartWorkspace (workspaceruntime.h)
description: Associates user credentials and certificates with a connection ID.
helpviewer_keywords: ["IWorkspaceScriptable interface [Remote Desktop Services]","StartWorkspace method","IWorkspaceScriptable.StartWorkspace","IWorkspaceScriptable2 interface [Remote Desktop Services]","StartWorkspace method","IWorkspaceScriptable2::StartWorkspace","IWorkspaceScriptable3 interface [Remote Desktop Services]","StartWorkspace method","IWorkspaceScriptable3::StartWorkspace","IWorkspaceScriptable::StartWorkspace","StartWorkspace","StartWorkspace method [Remote Desktop Services]","StartWorkspace method [Remote Desktop Services]","IWorkspaceScriptable interface","StartWorkspace method [Remote Desktop Services]","IWorkspaceScriptable2 interface","StartWorkspace method [Remote Desktop Services]","IWorkspaceScriptable3 interface","StartWorkspace method [Remote Desktop Services]","Workspace object","WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE","WKS_FLAG_CREDS_AUTHENTICATED","WKS_FLAG_PASSWORD_ENCRYPTED","Workspace object [Remote Desktop Services]","StartWorkspace method","termserv.iworkspacescriptable_startworkspace","workspaceruntime/IWorkspaceScriptable2::StartWorkspace","workspaceruntime/IWorkspaceScriptable3::StartWorkspace","workspaceruntime/IWorkspaceScriptable::StartWorkspace"]
old-location: termserv\iworkspacescriptable_startworkspace.htm
tech.root: TermServ
ms.assetid: a2985ae1-7874-43e8-b0d3-ef3f13ac2f8d
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable interface [Remote Desktop Services],StartWorkspace method, IWorkspaceScriptable.StartWorkspace, IWorkspaceScriptable2 interface [Remote Desktop Services],StartWorkspace method, IWorkspaceScriptable2::StartWorkspace, IWorkspaceScriptable3 interface [Remote Desktop Services],StartWorkspace method, IWorkspaceScriptable3::StartWorkspace, IWorkspaceScriptable::StartWorkspace, StartWorkspace, StartWorkspace method [Remote Desktop Services], StartWorkspace method [Remote Desktop Services],IWorkspaceScriptable interface, StartWorkspace method [Remote Desktop Services],IWorkspaceScriptable2 interface, StartWorkspace method [Remote Desktop Services],IWorkspaceScriptable3 interface, StartWorkspace method [Remote Desktop Services],Workspace object, WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE, WKS_FLAG_CREDS_AUTHENTICATED, WKS_FLAG_PASSWORD_ENCRYPTED, Workspace object [Remote Desktop Services],StartWorkspace method, termserv.iworkspacescriptable_startworkspace, workspaceruntime/IWorkspaceScriptable2::StartWorkspace, workspaceruntime/IWorkspaceScriptable3::StartWorkspace, workspaceruntime/IWorkspaceScriptable::StartWorkspace
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
 - IWorkspaceScriptable::StartWorkspace
 - workspaceruntime/IWorkspaceScriptable::StartWorkspace
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
 - IWorkspaceScriptable.StartWorkspace
 - IWorkspaceScriptable2.StartWorkspace
 - IWorkspaceScriptable3.StartWorkspace
 - Workspace.StartWorkspace
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

The user credentials are verified. If this flag is not set, you must call the <a href="/previous-versions/windows/desktop/legacy/ee351600(v=vs.85)">OnAuthenticated</a> method before using the credentials.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>