---
UID: NF:workspaceruntime.IWorkspaceScriptable2.StartWorkspaceEx
title: IWorkspaceScriptable2::StartWorkspaceEx (workspaceruntime.h)
description: Associates user credentials and certificates with a connection ID; also contains additional security and UI elements.
helpviewer_keywords: ["IWorkspaceScriptable2 interface [Remote Desktop Services]","StartWorkspaceEx method","IWorkspaceScriptable2.StartWorkspaceEx","IWorkspaceScriptable2::StartWorkspaceEx","IWorkspaceScriptable3 interface [Remote Desktop Services]","StartWorkspaceEx method","IWorkspaceScriptable3::StartWorkspaceEx","StartWorkspaceEx","StartWorkspaceEx method [Remote Desktop Services]","StartWorkspaceEx method [Remote Desktop Services]","IWorkspaceScriptable2 interface","StartWorkspaceEx method [Remote Desktop Services]","IWorkspaceScriptable3 interface","StartWorkspaceEx method [Remote Desktop Services]","Workspace object","WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE","WKS_FLAG_CREDS_AUTHENTICATED","WKS_FLAG_PASSWORD_ENCRYPTED","Workspace object [Remote Desktop Services]","StartWorkspaceEx method","termserv.iworkspacescriptable2_startworkspaceex","workspaceruntime/IWorkspaceScriptable2::StartWorkspaceEx","workspaceruntime/IWorkspaceScriptable3::StartWorkspaceEx"]
old-location: termserv\iworkspacescriptable2_startworkspaceex.htm
tech.root: TermServ
ms.assetid: 8383ee1c-ff6a-4251-8b0d-a2a8c0674873
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable2 interface [Remote Desktop Services],StartWorkspaceEx method, IWorkspaceScriptable2.StartWorkspaceEx, IWorkspaceScriptable2::StartWorkspaceEx, IWorkspaceScriptable3 interface [Remote Desktop Services],StartWorkspaceEx method, IWorkspaceScriptable3::StartWorkspaceEx, StartWorkspaceEx, StartWorkspaceEx method [Remote Desktop Services], StartWorkspaceEx method [Remote Desktop Services],IWorkspaceScriptable2 interface, StartWorkspaceEx method [Remote Desktop Services],IWorkspaceScriptable3 interface, StartWorkspaceEx method [Remote Desktop Services],Workspace object, WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE, WKS_FLAG_CREDS_AUTHENTICATED, WKS_FLAG_PASSWORD_ENCRYPTED, Workspace object [Remote Desktop Services],StartWorkspaceEx method, termserv.iworkspacescriptable2_startworkspaceex, workspaceruntime/IWorkspaceScriptable2::StartWorkspaceEx, workspaceruntime/IWorkspaceScriptable3::StartWorkspaceEx
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceScriptable2::StartWorkspaceEx
 - workspaceruntime/IWorkspaceScriptable2::StartWorkspaceEx
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
 - IWorkspaceScriptable2.StartWorkspaceEx
 - IWorkspaceScriptable3.StartWorkspaceEx
 - Workspace.StartWorkspaceEx
---

# IWorkspaceScriptable2::StartWorkspaceEx


## -description

Associates user credentials and certificates with a connection ID; also contains additional security and UI elements.

## -parameters

### -param bstrWorkspaceId [in]

A string that contains the connection ID.

### -param bstrWorkspaceFriendlyName [in]

The friendly name of the workspace to display in the UI.

### -param bstrRedirectorName [in]

String containing the name of the redirector.

### -param bstrUserName [in]

A string that contains a user name.

### -param bstrPassword [in]

A string that contains a password.

### -param bstrAppContainer [in]

A string containing the app container for the workspace.

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

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>