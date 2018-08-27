---
UID: NN:wsmandisp.IWSManConnectionOptions
title: IWSManConnectionOptions
author: windows-sdk-content
description: The ConnectionOptions object is passed to the CreateSession method to provide the user name and password associated with the local account on the remote computer.
old-location: winrm\connectionoptions.htm
old-project: winrm
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ConnectionOptions, ConnectionOptions object [Windows Remote Management], ConnectionOptions object [Windows Remote Management],described, IWSManConnectionOptions, winrm.connectionoptions, wsman.connectionoptions, wsmandisp/ConnectionOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsmandisp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - ConnectionOptions
 - IWSManConnectionOptions
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManConnectionOptions interface


## -description


The <b>ConnectionOptions</b> object is passed to the <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">CreateSession</a> method to provide the user name and password associated with the local account on the remote computer. If no parameters are supplied, then the credentials of the account running the script are set to the default values.


## -remarks



The <b>ConnectionOptions</b> object corresponds to the  <a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a> interface.

If a   Windows Remote Management client application  is running under impersonation, then a failure occurs if you set  the <a href="https://msdn.microsoft.com/61ba54b6-7da0-423e-b5b2-c4dd8aacd042">Password</a> property. A client application is a script or other program that sends a request to  WinRM on the local or a remote computer. The client application may be running under impersonation because it called a function like <a href="https://msdn.microsoft.com/ec814a85-4f93-4a25-82f0-ce83caf37e5d">ImpersonateClient</a>. An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.

The <b>WSManFlagCredUserNamePassword</b> flag should be set on the <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSman.CreateSession</a> call when using the <a href="https://msdn.microsoft.com/e8f70143-f002-4b39-97a3-006b9713262d">UserName</a> and <a href="https://msdn.microsoft.com/61ba54b6-7da0-423e-b5b2-c4dd8aacd042">Password</a> for authentication.


#### Examples

The following VBScript code example shows how to create a <b>ConnectionOptions</b> object, set the properties for the account on the remote computer, and use it in creating a <a href="https://msdn.microsoft.com/b98ca759-71cb-492e-8645-8766b202eb36">Session</a> object.


```vb
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```





## -see-also




<a href="https://msdn.microsoft.com/f58add53-0746-4423-9ab8-02ba05f82fa7">About Windows Remote Management</a>



<a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>



<a href="https://msdn.microsoft.com/578eee80-a6c1-4456-9683-14e0a3386248">Obtaining Data from a Remote Computer</a>



<a href="https://msdn.microsoft.com/7f08b557-bbd4-4f67-b5e5-b84e8af58657">Obtaining Data from the Local Computer</a>



<a href="https://msdn.microsoft.com/fda2042a-8fca-4cd8-bb55-fd1c3591921e">Scripting in Windows Remote Management</a>



<a href="https://msdn.microsoft.com/6ee2b238-5bc2-4274-b7ca-49dbc728d8f1">Using Windows Remote Management</a>



<a href="https://msdn.microsoft.com/bd642669-554f-40ab-bd40-235013afa077">WinRM Scripting API</a>
 

 

