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

# IServiceSxsConfig::SxsConfig


## -description


Configures the side-by-side assembly for the enclosed work.


## -parameters




### -param scsConfig [in]

A value from the <a href="https://msdn.microsoft.com/8c114e9e-b201-4317-8a45-d5b0964c6ff8">CSC_SxsConfig</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



The <a href="https://msdn.microsoft.com/5eb909a5-7730-4f0b-aee6-9bb8de076cea">SxsDirectory</a> method must be called if a new side-by-side assembly domain is created using a call to this method.





## -see-also




<a href="https://msdn.microsoft.com/24d4a22b-0a01-4bf2-9cc6-4a1b31897d05">IServiceSxsConfig</a>
 

 

