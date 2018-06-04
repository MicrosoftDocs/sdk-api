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

# SfcIsFileProtected function


## -description


Determines whether the specified file is protected. Applications should avoid replacing protected system files.


## -parameters




### -param RpcHandle [in]

This parameter must be <b>NULL</b>.


### -param ProtFileName [in]

The name of the file.


## -returns



If the file is protected, the return value is a nonzero value.

If the file is not protected, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/6e26a539-a22a-487a-b720-fa3660c1b485">SfcIsKeyProtected</a>
 

 

