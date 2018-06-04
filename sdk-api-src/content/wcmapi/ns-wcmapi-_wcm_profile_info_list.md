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

# _WCM_PROFILE_INFO_LIST structure


## -description


The <b>WCM_PROFILE_INFO_LIST</b> structure contains a list of profiles in preferred order.


## -struct-fields




### -field dwNumberOfItems

Type: <b>DWORD</b>

The number of profiles in the list.


### -field ProfileInfo.unique

 


### -field ProfileInfo.size_is

 


### -field ProfileInfo.size_is.dwNumberOfItems

 


### -field ProfileInfo

Type: <b><a href="https://msdn.microsoft.com/bf917afa-c6c5-408a-bd34-b4a4c7b991b9">WCM_PROFILE_INFO</a>[1]</b>

Information about each profile.


## -see-also




<a href="https://msdn.microsoft.com/bf917afa-c6c5-408a-bd34-b4a4c7b991b9">WCM_PROFILE_INFO</a>
 

 

