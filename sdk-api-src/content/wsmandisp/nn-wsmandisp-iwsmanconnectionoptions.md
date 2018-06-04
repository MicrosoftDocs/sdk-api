---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWSManConnectionOptions interface


## -description


The <b>IWSManConnectionOptions</b> object is passed to the <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a> method to provide the user name and password associated with the local account on the remote computer. If no parameters are supplied, then the credentials of the account running the script are the default values.


## -remarks



If a   Windows Remote Management client application  is running under impersonation, then a failure occurs if you set  the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915695">Password</a> property. A client application is a script or other program that sends a request to  WinRM on the local or a remote computer. The client application may be running under impersonation because it called a function like <a href="https://msdn.microsoft.com/ec814a85-4f93-4a25-82f0-ce83caf37e5d">ImpersonateClient</a>. An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.




## -see-also




<a href="https://msdn.microsoft.com/7a87a5f7-78ed-452c-9b9f-ad48811a3339">ConnectionOptions</a>



<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

