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

# FreeMemoryJobObject function


## -description


Frees memory that a function related to job objects allocated. Functions related to job objects that allocate memory include <a href="https://msdn.microsoft.com/B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC">QueryIoRateControlInformationJobObject</a>.  


## -parameters




### -param Buffer [in]

A pointer to the buffer of allocated memory that you want to free.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC">QueryIoRateControlInformationJobObject</a>
 

 

