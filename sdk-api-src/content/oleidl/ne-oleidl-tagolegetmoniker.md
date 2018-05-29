---
UID: NE:oleidl.tagOLEGETMONIKER
title: tagOLEGETMONIKER
author: windows-sdk-content
description: Controls aspects of the behavior of the IOleObject::GetMoniker and IOleClientSite::GetMoniker methods.
old-location: com\olegetmoniker.htm
old-project: com
ms.assetid: b69e3213-08c4-45f8-b1b3-4ca78e966251
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: OLEGETMONIKER, OLEGETMONIKER enumeration [COM], OLEGETMONIKER_FORCEASSIGN, OLEGETMONIKER_ONLYIFTHERE, OLEGETMONIKER_TEMPFORUSER, OLEGETMONIKER_UNASSIGN, _ole_OLEGETMONIKER, com.olegetmoniker, oleidl/OLEGETMONIKER, oleidl/OLEGETMONIKER_FORCEASSIGN, oleidl/OLEGETMONIKER_ONLYIFTHERE, oleidl/OLEGETMONIKER_TEMPFORUSER, oleidl/OLEGETMONIKER_UNASSIGN, tagOLEGETMONIKER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIVIEWPROPSW (Unicode) and OLEUIVIEWPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OLEGETMONIKER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OleIdl.h
api_name:
-	OLEGETMONIKER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

