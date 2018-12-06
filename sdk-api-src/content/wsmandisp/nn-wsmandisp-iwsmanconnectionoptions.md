---
UID: NN:wsmandisp.IWSManConnectionOptions
title: IWSManConnectionOptions
author: windows-sdk-content
description: The IWSManConnectionOptions object is passed to the IWSMan::CreateSession method to provide the user name and password associated with the local account on the remote computer.
old-location: winrm\iwsmanconnectionoptions.htm
tech.root: winrm
ms.assetid: 940097da-c5bb-4170-a2aa-fcbbee622fe6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSManConnectionOptions, IWSManConnectionOptions interface [Windows Remote Management], IWSManConnectionOptions interface [Windows Remote Management],described, winrm.iwsmanconnectionoptions, wsmandisp/IWSManConnectionOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wsmandisp.h
req.include-header: 
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
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManConnectionOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManConnectionOptions interface


## -description


The <b>IWSManConnectionOptions</b> object is passed to the <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a> method to provide the user name and password associated with the local account on the remote computer. If no parameters are supplied, then the credentials of the account running the script are the default values.


## -remarks



If a   Windows Remote Management client application  is running under impersonation, then a failure occurs if you set  the <a href="https://msdn.microsoft.com/61ba54b6-7da0-423e-b5b2-c4dd8aacd042">Password</a> property. A client application is a script or other program that sends a request to  WinRM on the local or a remote computer. The client application may be running under impersonation because it called a function like <a href="https://msdn.microsoft.com/ec814a85-4f93-4a25-82f0-ce83caf37e5d">ImpersonateClient</a>. An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.




## -see-also




<a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a>



<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

