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

# WcmSetProfileList function


## -description


The <b>WcmSetProfileList</b> function reorders a profile list or a subset of a profile list.


## -parameters




### -param pProfileList [in]

Type: <b><a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">WCM_PROFILE_INFO_LIST</a>*</b>

The list of profiles to be reordered, provided in the preferred order (descending from the most preferred to the least preferred).


### -param dwPosition [in]

Type: <b>DWORD</b>

Specifies the position in the list to start the reorder.


### -param fIgnoreUnknownProfiles [in]

Type: <b>BOOL</b>

True if any profiles in <i>pProfileList</i> which do not exist should be ignored; the call will proceed with the remainder of the list. False if the call should fail without modifying the profile order if any profiles in <i>pProfileList</i> do not exist.


### -param pReserved

Type: <b>PVOID</b>

Reserved.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/73ddb610-233a-470b-900d-ae62a1e7121a">WCM_PROFILE_INFO_LIST</a>
 

 

