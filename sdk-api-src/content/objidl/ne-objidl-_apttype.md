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

# _APTTYPE enumeration


## -description


Specifies different types of apartments.


## -enum-fields




### -field APTTYPE_CURRENT

The current thread.


### -field APTTYPE_STA

A single-threaded apartment.


### -field APTTYPE_MTA

A multithreaded apartment.


### -field APTTYPE_NA

A neutral apartment.


### -field APTTYPE_MAINSTA

The main single-threaded apartment.


## -see-also




<a href="https://msdn.microsoft.com/ab0b6008-397f-4210-ba26-1a041b709722">CoGetApartmentType</a>



<a href="https://msdn.microsoft.com/59cb216f-818c-4189-b77b-984961889a62">IComThreadingInfo::GetCurrentApartmentType</a>
 

 

