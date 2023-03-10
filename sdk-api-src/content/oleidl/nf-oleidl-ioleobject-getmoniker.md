---
UID: NF:oleidl.IOleObject.GetMoniker
title: IOleObject::GetMoniker (oleidl.h)
description: Retrieves an embedded object's moniker, which the caller can use to link to the object.
helpviewer_keywords: ["GetMoniker","GetMoniker method [COM]","GetMoniker method [COM]","IOleObject interface","IOleObject interface [COM]","GetMoniker method","IOleObject.GetMoniker","IOleObject::GetMoniker","_ole_ioleobject_getmoniker","com.ioleobject_getmoniker","oleidl/IOleObject::GetMoniker"]
old-location: com\ioleobject_getmoniker.htm
tech.root: com
ms.assetid: 6b81ca75-31d8-45d6-8b36-663c5f19341c
ms.date: 12/05/2018
ms.keywords: GetMoniker, GetMoniker method [COM], GetMoniker method [COM],IOleObject interface, IOleObject interface [COM],GetMoniker method, IOleObject.GetMoniker, IOleObject::GetMoniker, _ole_ioleobject_getmoniker, com.ioleobject_getmoniker, oleidl/IOleObject::GetMoniker
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
 - IOleObject::GetMoniker
 - oleidl/IOleObject::GetMoniker
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
 - IOleObject.GetMoniker
---

# IOleObject::GetMoniker


## -description

Retrieves an embedded object's moniker, which the caller can use to link to the object.

## -parameters

### -param dwAssign [in]

Determines how the moniker is assigned to the object. Depending on the value of <i>dwAssign</i>, <b>IOleObject::GetMoniker</b> does one of the following:

<ul>
<li>Obtains a moniker only if one has already been assigned.</li>
<li>Forces assignment of a moniker, if necessary, in order to satisfy the call.</li>
<li>Obtains a temporary moniker.</li>
</ul>
Values for <i>dwAssign</i> are specified in the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olegetmoniker">OLEGETMONIKER</a>.

<div class="alert"><b>Note</b>   You cannot pass <a href="/windows/desktop/api/oleidl/ne-oleidl-olegetmoniker">OLEGETMONIKER</a>_UNASSIGN when calling <b>IOleObject::GetMoniker</b>. This value is valid only when calling <b>IOleObject::GetMoniker</b>.</div>
<div> </div>

### -param dwWhichMoniker [in]

Specifies the form of the moniker being requested. Possible values are taken from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olewhichmk">OLEWHICHMK</a>.

### -param ppmk [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the interface pointer to the object's moniker. If an error occurs, <i>ppmk</i> must be set to <b>NULL</b>. Each time an object receives a call to <b>IOleObject::GetMoniker</b>, it must increase the reference count on <i>ppmk</i>. It is the caller's responsibility to call Release when it is done with <i>ppmk</i>.

## -returns

This method returns S_OK on success.

## -remarks

The <b>IOleObject::GetMoniker</b> method returns an object's moniker. Like <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>, this method is important only in the context of managing links to embedded objects and even in that case is optional. A potential link client that requires an object's moniker to bind to the object can call this method to obtain that moniker. The default implementation of <b>IOleObject::GetMoniker</b> calls the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>, returning E_UNEXPECTED if the object is not running or does not have a valid pointer to a client site.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createitemmoniker">CreateItemMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olegetmoniker">OLEGETMONIKER</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olewhichmk">OLEWHICHMK</a>