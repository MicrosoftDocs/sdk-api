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

# RoGetApartmentIdentifier function


## -description


Gets a unique identifier for the current apartment.


## -parameters




### -param apartmentIdentifier [out]

A process-unique identifier for the current apartment.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a>



<a href="https://msdn.microsoft.com/DE0C79AD-D80F-44EE-A628-147FC8474905">RoRegisterForApartmentShutdown</a>



<a href="https://msdn.microsoft.com/B6E22C50-14EC-4B0F-8C97-7D1062BF6072">RoUnregisterForApartmentShutdown</a>
 

 

