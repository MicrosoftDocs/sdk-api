---
UID: NF:oleidl.IOleObject.GetClientSite
title: IOleObject::GetClientSite
author: windows-sdk-content
description: Retrieves a pointer to an embedded object's client site.
old-location: com\ioleobject_getclientsite.htm
old-project: com
ms.assetid: bf26b989-445c-48d3-b279-29e4cef0ad97
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetClientSite, GetClientSite method [COM], GetClientSite method [COM],IOleObject interface, IOleObject interface [COM],GetClientSite method, IOleObject.GetClientSite, IOleObject::GetClientSite, _ole_ioleobject_getclientsite, com.ioleobject_getclientsite, oleidl/IOleObject::GetClientSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleObject.GetClientSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleObject::GetClientSite


## -description


Retrieves a pointer to an embedded object's client site.


## -parameters




### -param ppClientSite [out]

Address of <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> pointer variable that receives the interface pointer to the object's client site. If an object does not yet know its client site, or if an error has occurred, <i>ppClientSite</i> must be set to <b>NULL</b>. Each time an object receives a call to <b>IOleObject::GetClientSite</b>, it must increase the reference count on <i>ppClientSite</i>. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> when it is done with <i>ppClientSite</i>.


## -returns



This method returns S_OK on success.




## -remarks



Link clients most commonly call the <b>IOleObject::GetClientSite</b> method in conjunction with the <a href="https://msdn.microsoft.com/8f0caf07-f059-4e0c-9c28-c7ad0cc149e3">IOleClientSite::GetContainer</a> method to traverse a hierarchy of nested objects. A link client calls <b>IOleObject::GetClientSite</b> to get a pointer to the link source's client site. The client then calls <b>IOleClientSite::GetContainer</b> to get a pointer to the link source's container. Finally, the client calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to get <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> and <b>IOleObject::GetClientSite</b> to get the container's client site within its container. By repeating this sequence of calls, the caller can eventually retrieve a pointer to the master container in which all the other objects are nested.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The returned client-site pointer will be <b>NULL</b> if an embedded object has not yet been informed of its client site. This will be the case with a newly loaded or created object when a container has passed a <b>NULL</b> client-site pointer to one of the object-creation helper functions but has not yet called <a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a> as part of initializing the object.




## -see-also




<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a>
 

 

