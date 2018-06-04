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

# IOleUILinkContainerW::GetNextLink


## -description


Enumerates the links in a container.


## -parameters




### -param dwLink [in]

Container-defined unique identifier for a single link. This value is only passed to other methods on this interface, so it can be any value that uniquely identifies a link to the container. Containers frequently use the pointer to the link's container site object for this value.


## -returns



Returns a container's link identifiers in sequence; <b>NULL</b> if it has returned the last link.




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method to enumerate the links in a container. If the value passed in <i>dwLink</i> is <b>NULL</b>, then the container should return the first link's identifier. If <i>dwLink</i> identifies the last link in the container, then the container should return <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/136894a6-ddf6-4a47-80f5-997625362536">IOleUILinkContainer::GetLinkUpdateOptions</a>



<a href="https://msdn.microsoft.com/d2a7758d-9692-4e3c-8186-b74530299a6a">IOleUILinkContainer::SetLinkUpdateOptions</a>
 

 

