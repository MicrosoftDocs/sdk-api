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

# OpenResourceManager function


## -description


Opens an existing resource manager (RM).


## -parameters




### -param dwDesiredAccess [in]

The access requested for the RM. See <a href="https://msdn.microsoft.com/6b901b73-516d-4f27-b258-3b93a8f9675f">Resource Manager Access Masks</a> for a list of valid values.


### -param TmHandle [in]

A handle to the transaction manager.


### -param ResourceManagerId

TBD




#### - RmGuid [in]

The identifier  for this resource manager.


## -returns



If the function succeeds, the return value is a handle to the resource manager.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the  possible error codes:




## -remarks



Immediately after calling this function, you must call <a href="https://msdn.microsoft.com/616ff873-c0d0-464e-9b1b-74a426b99abd">RecoverResourceManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/ad88e478-1dff-4f35-a0e3-6bda8bb45711">CreateResourceManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/6b901b73-516d-4f27-b258-3b93a8f9675f">Resource Manager Access Masks</a>
 

 

