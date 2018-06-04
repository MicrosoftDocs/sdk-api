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

# SysFreeString function


## -description


Deallocates a string allocated previously by <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>, <a href="https://msdn.microsoft.com/e7f49441-eff1-4c00-b61f-8522c4e250ef">SysAllocStringByteLen</a>, <a href="https://msdn.microsoft.com/0207c33b-c065-42bb-8d70-ccdc3fddb338">SysReAllocString</a>, <a href="https://msdn.microsoft.com/f98bff39-bc5f-4a81-85d7-d5228e20fbc8">SysAllocStringLen</a>, or <a href="https://msdn.microsoft.com/d134cff1-7cc8-4284-a216-3819615e3017">SysReAllocStringLen</a>.


## -parameters




### -param bstrString [in, optional]

The previously allocated string. If this parameter is <b>NULL</b>, the function simply returns.


## -returns



This function does not return a value.



