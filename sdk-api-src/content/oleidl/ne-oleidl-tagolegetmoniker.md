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

# tagOLEGETMONIKER enumeration


## -description


Controls aspects of the behavior of the <a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">IOleObject::GetMoniker</a> and <a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a> methods.


## -enum-fields




### -field OLEGETMONIKER_ONLYIFTHERE

If a moniker for the object or container does not exist, <a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a> should return E_FAIL and not assign a moniker.


### -field OLEGETMONIKER_FORCEASSIGN

If a moniker for the object or container does not exist, <a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a> should create one. 


### -field OLEGETMONIKER_UNASSIGN


<a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a> can release the object's moniker (although it is not required to do so). This constant is not valid in <a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">IOleObject::GetMoniker</a>. 


### -field OLEGETMONIKER_TEMPFORUSER

If a moniker for the object does not exist, <a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">IOleObject::GetMoniker</a> can create a temporary moniker that can be used for display purposes (<a href="https://msdn.microsoft.com/424036c9-c097-4507-b562-4a01f9199b1f">IMoniker::GetDisplayName</a>) but not for binding. This enables the object server to return a descriptive name for the object without incurring the overhead of creating and maintaining a moniker until a link is actually created. 



## -remarks



If the OLEGETMONIKER_FORCEASSIGN flag causes a container to create a moniker for the object, the container should notify the object by calling the <a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">IOleObject::GetMoniker</a> method.





## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a>



<a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">IOleObject::GetMoniker</a>
 

 

