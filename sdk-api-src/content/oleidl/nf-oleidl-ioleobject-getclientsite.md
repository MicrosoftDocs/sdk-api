---
UID: NF:oleidl.IOleObject.GetClientSite
title: IOleObject::GetClientSite (oleidl.h)
description: Retrieves a pointer to an embedded object's client site.
helpviewer_keywords: ["GetClientSite","GetClientSite method [COM]","GetClientSite method [COM]","IOleObject interface","IOleObject interface [COM]","GetClientSite method","IOleObject.GetClientSite","IOleObject::GetClientSite","_ole_ioleobject_getclientsite","com.ioleobject_getclientsite","oleidl/IOleObject::GetClientSite"]
old-location: com\ioleobject_getclientsite.htm
tech.root: com
ms.assetid: bf26b989-445c-48d3-b279-29e4cef0ad97
ms.date: 12/05/2018
ms.keywords: GetClientSite, GetClientSite method [COM], GetClientSite method [COM],IOleObject interface, IOleObject interface [COM],GetClientSite method, IOleObject.GetClientSite, IOleObject::GetClientSite, _ole_ioleobject_getclientsite, com.ioleobject_getclientsite, oleidl/IOleObject::GetClientSite
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleObject::GetClientSite
 - oleidl/IOleObject::GetClientSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.GetClientSite
---

# IOleObject::GetClientSite


## -description

Retrieves a pointer to an embedded object's client site.

## -parameters

### -param ppClientSite [out]

Address of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> pointer variable that receives the interface pointer to the object's client site. If an object does not yet know its client site, or if an error has occurred, <i>ppClientSite</i> must be set to <b>NULL</b>. Each time an object receives a call to <b>IOleObject::GetClientSite</b>, it must increase the reference count on <i>ppClientSite</i>. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when it is done with <i>ppClientSite</i>.

## -returns

This method returns S_OK on success.

## -remarks

Link clients most commonly call the <b>IOleObject::GetClientSite</b> method in conjunction with the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getcontainer">IOleClientSite::GetContainer</a> method to traverse a hierarchy of nested objects. A link client calls <b>IOleObject::GetClientSite</b> to get a pointer to the link source's client site. The client then calls <b>IOleClientSite::GetContainer</b> to get a pointer to the link source's container. Finally, the client calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to get <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> and <b>IOleObject::GetClientSite</b> to get the container's client site within its container. By repeating this sequence of calls, the caller can eventually retrieve a pointer to the master container in which all the other objects are nested.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The returned client-site pointer will be <b>NULL</b> if an embedded object has not yet been informed of its client site. This will be the case with a newly loaded or created object when a container has passed a <b>NULL</b> client-site pointer to one of the object-creation helper functions but has not yet called <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a> as part of initializing the object.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a>