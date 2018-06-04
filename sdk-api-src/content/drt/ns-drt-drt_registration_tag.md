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

# drt_registration_tag structure


## -description


The <b>DRT_REGISTRATION</b> structure contains  key and application data that make up a registration.


## -struct-fields




### -field key

Contains the key portion of the registration.


### -field appData

The application data associated with the key. The <a href="https://msdn.microsoft.com/ee81daca-e889-471e-b43b-4593380a55dd">DRT_DATA</a> structure containing this application data must point to a buffer less than 4KB in size.


## -see-also




<a href="https://msdn.microsoft.com/23cf713e-2730-456c-a3da-649c5ed00ffb">DRT_SEARCH_RESULT</a>



<a href="https://msdn.microsoft.com/069358e0-4b61-44ed-b235-37f1d038feff">DrtCreateDerivedKey</a>



<a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a>
 

 

