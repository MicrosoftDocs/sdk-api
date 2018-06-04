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

# LsaQueryCAPs function


## -description


Returns the Central Access Policies (CAPs) for the specified IDs.


## -parameters




### -param CAPIDs

A pointer to a variable that contains an array of pointers to CAPIDs that identify the CAPs being queried.


### -param CAPIDCount [in]

The number of IDs in the <i>CAPIDs</i> parameter.


### -param CAPs [out]

Receives a pointer to an array of pointers to <a href="https://msdn.microsoft.com/C1C2E8AE-0B7F-4620-9C27-31DAF683E342">CENTRAL_ACCESS_POLICY</a> structures representing the queried CAPs.


### -param CAPCount [out]

The number of <a href="https://msdn.microsoft.com/C1C2E8AE-0B7F-4620-9C27-31DAF683E342">CENTRAL_ACCESS_POLICY</a> structure pointers returned in the <i>CAPs</i> parameter.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the <a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.



