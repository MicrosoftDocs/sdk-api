---
UID: NF:oleidl.IOleClientSite.GetMoniker
title: IOleClientSite::GetMoniker (oleidl.h)
description: Retrieves a moniker for the object's client site. An object can force the assignment of its own or its container's moniker by specifying a value for dwAssign.
helpviewer_keywords: ["GetMoniker","GetMoniker method [COM]","GetMoniker method [COM]","IOleClientSite interface","IOleClientSite interface [COM]","GetMoniker method","IOleClientSite.GetMoniker","IOleClientSite::GetMoniker","_ole_ioleclientsite_getmoniker","com.ioleclientsite_getmoniker","oleidl/IOleClientSite::GetMoniker"]
old-location: com\ioleclientsite_getmoniker.htm
tech.root: com
ms.assetid: 9ca3e997-9a96-43c3-a213-de8c8440cd54
ms.date: 12/05/2018
ms.keywords: GetMoniker, GetMoniker method [COM], GetMoniker method [COM],IOleClientSite interface, IOleClientSite interface [COM],GetMoniker method, IOleClientSite.GetMoniker, IOleClientSite::GetMoniker, _ole_ioleclientsite_getmoniker, com.ioleclientsite_getmoniker, oleidl/IOleClientSite::GetMoniker
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
 - IOleClientSite::GetMoniker
 - oleidl/IOleClientSite::GetMoniker
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
 - IOleClientSite.GetMoniker
---

# IOleClientSite::GetMoniker


## -description

Retrieves a moniker for the object's client site. An object can force the assignment of its own or its container's moniker by specifying a value for <i>dwAssign</i>.

## -parameters

### -param dwAssign [in]

Specifies whether to get a moniker only if one already exists, force assignment of a moniker, create a temporary moniker, or remove a moniker that has been assigned. In practice, you will usually request that the container force assignment of the moniker. Possible values are taken from the <a href="/windows/desktop/api/oleidl/ne-oleidl-olegetmoniker">OLEGETMONIKER</a> enumeration.

### -param dwWhichMoniker [in]

Specifies whether to return the container's moniker, the object's moniker relative to the container, or the object's full moniker. In practice, you will usually request the object's full moniker. Possible values are taken from the <a href="/windows/desktop/api/oleidl/ne-oleidl-olewhichmk">OLEWHICHMK</a> enumeration.

### -param ppmk [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer variable that receives the interface pointer to the moniker for the object's client site. If an error occurs, the implementation must set <i>ppmk</i> to <b>NULL</b>. Each time a container receives a call to <b>IOleClientSite::GetMoniker</b>, it must increase the reference count on the <i>ppmk</i> pointer it returns. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when it is finished with the pointer.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This container cannot assign monikers to objects. This is the case with OLE 1 containers.

</td>
</tr>
</table>

## -remarks

Containers implement <b>GetMoniker</b> as a way of passing out monikers for their embedded objects to clients that need to link to those objects.

When a link is made to an embedded object or to a pseudo-object within it (a range of cells in a spreadsheet, for example), the object needs a moniker to construct the composite moniker indicating the source of the link. If the embedded object does not already have a moniker, it can call <b>GetMoniker</b> to request one.

Every container that expects to contain links to embeddings should support <b>GetMoniker</b> to give out OLEWHICHMK_CONTAINER, thus enabling link tracking when the link client and link source files move, but maintain the same relative position.

An object must not persistently store its full moniker or its container's moniker, because these can change while the object is not loaded. For example, either the container or the object could be renamed, in which event, storing the container's moniker or the object's full moniker would make it impossible for a client to track a link to the object.

In some very specialized cases, an object may no longer need a moniker previously assigned to it and may wish to have it removed as an optimization. In such cases, the object can call <b>GetMoniker</b> with OLEGETMONIKER_UNASSIGN to have the moniker removed.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>