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

# TdhCloseDecodingHandle function


## -description


Frees any resources associated with the input decoding handle.


## -parameters




### -param Handle [in]

Type: <b>TDH_HANDLE</b>

The decoding handle to be closed.


## -returns



Type: <b>ULONG</b>

This function returns ERROR_SUCCESS on completion.




## -see-also




<a href="https://msdn.microsoft.com/ea437d31-a688-4602-8453-f891e83af9ea">TdhOpenDecodingHandle</a>
 

 

