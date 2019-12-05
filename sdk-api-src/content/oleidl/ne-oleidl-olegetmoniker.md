---
UID: NE:oleidl.tagOLEGETMONIKER
title: OLEGETMONIKER (oleidl.h)
description: Controls aspects of the behavior of the IOleObject::GetMoniker and IOleClientSite::GetMoniker methods.
old-location: com\olegetmoniker.htm
tech.root: com
ms.assetid: b69e3213-08c4-45f8-b1b3-4ca78e966251
ms.date: 12/05/2018
ms.keywords: OLEGETMONIKER, OLEGETMONIKER enumeration [COM], OLEGETMONIKER_FORCEASSIGN, OLEGETMONIKER_ONLYIFTHERE, OLEGETMONIKER_TEMPFORUSER, OLEGETMONIKER_UNASSIGN, _ole_OLEGETMONIKER, com.olegetmoniker, oleidl/OLEGETMONIKER, oleidl/OLEGETMONIKER_FORCEASSIGN, oleidl/OLEGETMONIKER_ONLYIFTHERE, oleidl/OLEGETMONIKER_TEMPFORUSER, oleidl/OLEGETMONIKER_UNASSIGN
ms.topic: enum
f1_keywords:
- oleidl/OLEGETMONIKER
dev_langs:
- c++
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- OleIdl.h
api_name:
- OLEGETMONIKER
targetos: Windows
req.typenames: OLEGETMONIKER
req.redist: 
ms.custom: 19H1
---

# OLEGETMONIKER enumeration


## -description


Controls aspects of the behavior of the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a> and <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a> methods.


## -enum-fields




### -field OLEGETMONIKER_ONLYIFTHERE

If a moniker for the object or container does not exist, <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a> should return E_FAIL and not assign a moniker.


### -field OLEGETMONIKER_FORCEASSIGN

If a moniker for the object or container does not exist, <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a> should create one. 


### -field OLEGETMONIKER_UNASSIGN


<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a> can release the object's moniker (although it is not required to do so). This constant is not valid in <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a>. 


### -field OLEGETMONIKER_TEMPFORUSER

If a moniker for the object does not exist, <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a> can create a temporary moniker that can be used for display purposes (<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-getdisplayname">IMoniker::GetDisplayName</a>) but not for binding. This enables the object server to return a descriptive name for the object without incurring the overhead of creating and maintaining a moniker until a link is actually created. 



## -remarks



If the OLEGETMONIKER_FORCEASSIGN flag causes a container to create a moniker for the object, the container should notify the object by calling the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a> method.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">IOleObject::GetMoniker</a>
 

 

