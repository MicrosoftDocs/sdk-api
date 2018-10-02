---
UID: NF:workspaceruntime.IWorkspaceScriptable3.StartWorkspaceEx2
title: IWorkspaceScriptable3::StartWorkspaceEx2
author: windows-sdk-content
description: Not implemented.
old-location: termserv\iworkspacescriptable3_startworkspaceex2.htm
tech.root: TermServ
ms.assetid: 819eb47e-f697-4b34-a91f-44aa95cf116a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWorkspaceScriptable3 interface [Remote Desktop Services],StartWorkspaceEx2 method, IWorkspaceScriptable3.StartWorkspaceEx2, IWorkspaceScriptable3::StartWorkspaceEx2, StartWorkspaceEx2, StartWorkspaceEx2 method [Remote Desktop Services], StartWorkspaceEx2 method [Remote Desktop Services],IWorkspaceScriptable3 interface, StartWorkspaceEx2 method [Remote Desktop Services],Workspace object, WKS_FLAG_CLEAR_CREDS_ON_LAST_RESOURCE, WKS_FLAG_CREDS_AUTHENTICATED, WKS_FLAG_PASSWORD_ENCRYPTED, Workspace object [Remote Desktop Services],StartWorkspaceEx2 method, termserv.iworkspacescriptable3_startworkspaceex2, workspaceruntime/IWorkspaceScriptable3::StartWorkspaceEx2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: workspaceruntime.h
req.include-header: Workspaceruntime.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - IWorkspaceScriptable3::StartWorkspaceEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceScriptable3::StartWorkspaceEx2


## -description


Not implemented.

Associates user credentials and certificates with a connection ID.


## -parameters




### -param bstrWorkspaceId [in]

A string that contains the connection ID.


### -param bstrWorkspaceFriendlyName [in] [in]

TBD


### -param bstrRedirectorName [in] [in]

TBD


### -param bstrUserName [in]

A string that contains a user name.


### -param bstrPassword [in]

A string that contains a password.


### -param bstrAppContainer [in] [in]

TBD


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


### -param bstrEventLogUploadAddress [in] [in]

TBD


### -param correlationId [in] [in]

TBD


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list.




## -see-also




<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

