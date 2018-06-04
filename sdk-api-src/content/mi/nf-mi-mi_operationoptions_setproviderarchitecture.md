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

# MI_OperationOptions_SetProviderArchitecture function


## -description


Sets the provider architecture for an operation.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param architecture [in]

One of the following <a href="https://msdn.microsoft.com/9dd275aa-23a9-44f4-916f-355b77490161">MI_ProviderArchitecture</a> values.



#### MI_PROVIDER_ARCHITECTURE_32BIT (0)

32-bit architecture.



#### MI_PROVIDER_ARCHITECTURE_64BIT (1)

64-bit architecture.


### -param mustComply [in]

Boolean value where <b>MI_TRUE</b> means that if you are asking for a 32-bit provider on a 64-bit machine, then a 32-bit provider must be used.  <b>MI_FALSE</b> means that a 64-bit provider can be used if a 32-bit provider is not available.


## -returns



This function returns MI_INLINE MI_Result.



