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

# DhcpRpcFreeMemory function


## -description



      The <b>DhcpRpcFreeMemory</b> function frees a block of buffer space returned as a parameter.


## -parameters




### -param BufferPointer

Pointer to an address that contains a structure (or structures, in the case of an array) returned as a parameter. 


## -returns



This function does not return a value.




## -remarks



This function should be called to release the memory consumed by any structures.



