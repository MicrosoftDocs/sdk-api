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

# OpenEnlistment function


## -description


Opens an existing enlistment object, and returns a handle to the enlistment.


## -parameters




### -param dwDesiredAccess [in]

The access requested for this enlistment. See <a href="https://msdn.microsoft.com/93773eb7-141a-49f3-9306-ffbda2f4ab9f">Enlistment Access Masks</a> for a list of valid values.


### -param ResourceManagerHandle [in]

A handle to the resource manager.


### -param EnlistmentId [in]

The enlistment identifier.


## -returns



If the function succeeds, the return value is a handle to the enlistment.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/7bc06468-947f-48ec-8e58-20df58ed93bd">CreateEnlistment</a>



<a href="https://msdn.microsoft.com/93773eb7-141a-49f3-9306-ffbda2f4ab9f">Enlistment Access Masks</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

