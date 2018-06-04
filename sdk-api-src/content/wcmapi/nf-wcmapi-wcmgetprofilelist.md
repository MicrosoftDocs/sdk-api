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

# WcmGetProfileList function


## -description


The <b>WcmGetProfileList</b> function retrieves a list of profiles in preferred order, descending from the most preferred to the least preferred. The list includes all WCM-managed auto-connect profiles across all WCM-managed media types.


## -parameters




### -param pReserved

Type: <b>PVOID</b>

Reserved.


### -param ppProfileList [out]

Type: <b><a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">PWCM_PROFILE_INFO_LIST</a>*</b>

The list of profiles.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">PWCM_PROFILE_INFO_LIST</a>
 

 

