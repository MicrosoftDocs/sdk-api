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

# MI_Filter_Evaluate function


## -description


The provider calls this function to evaluate an instance against a given filter.


## -parameters




### -param self [in]

This is a pointer to the filter the instance will be evaluated against.


### -param instance [in]

This is a pointer to the instance to evaluate.


### -param result [out]

When the API completes, result indicates whether the instance matched the filter.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.



