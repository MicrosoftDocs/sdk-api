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

# IX509PrivateKey::get_DefaultContainer


## -description


The <b>DefaultContainer</b> property retrieves a Boolean value that specifies whether the private key represents the default key container.

This property is read-only.


## -parameters


## -remarks



Key containers are identified by name. The name can be specified by the client, or it can be a default value supported by the CSP or KSP. For example, some CSPs use the logon name of the current user as the default container name.

This property value is set when the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> or <a href="https://msdn.microsoft.com/e8c6564a-6009-437e-9b83-3711e43a7374">Create</a> methods are called.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

