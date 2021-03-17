---
UID: NF:oleidl.IOleObject.EnumAdvise
title: IOleObject::EnumAdvise (oleidl.h)
description: Retrieves a pointer to an enumerator that can be used to enumerate the advisory connections registered for an object, so a container can know what to release prior to closing down.
helpviewer_keywords: ["EnumAdvise","EnumAdvise method [COM]","EnumAdvise method [COM]","IOleObject interface","IOleObject interface [COM]","EnumAdvise method","IOleObject.EnumAdvise","IOleObject::EnumAdvise","_ole_ioleobject_enumadvise","com.ioleobject_enumadvise","oleidl/IOleObject::EnumAdvise"]
old-location: com\ioleobject_enumadvise.htm
tech.root: com
ms.assetid: 4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc
ms.date: 12/05/2018
ms.keywords: EnumAdvise, EnumAdvise method [COM], EnumAdvise method [COM],IOleObject interface, IOleObject interface [COM],EnumAdvise method, IOleObject.EnumAdvise, IOleObject::EnumAdvise, _ole_ioleobject_enumadvise, com.ioleobject_enumadvise, oleidl/IOleObject::EnumAdvise
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
 - IOleObject::EnumAdvise
 - oleidl/IOleObject::EnumAdvise
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
 - IOleObject.EnumAdvise
---

# IOleObject::EnumAdvise


## -description

Retrieves a pointer to an enumerator that can be used to enumerate the advisory connections registered for an object, so a container can know what to release prior to closing down.

## -parameters

### -param ppenumAdvise [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the enumerator object. If the object does not have any advisory connections or if an error occurs, the implementation must set <i>ppenumAdvise</i> to <b>NULL</b>. Each time an object receives a successful call to <b>IOleObject::EnumAdvise</b>, it must increase the reference count on <i>ppenumAdvise</i>. It is the caller's responsibility to call Release when it is done with the <i>ppenumAdvise</i>.

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

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise">IOleObject::EnumAdvise</a> is not implemented.

</td>
</tr>
</table>

## -remarks

The <b>IOleObject::EnumAdvise</b> method supplies an enumerator that provides a way for containers to keep track of advisory connections registered for their objects. A container normally would call this function so that it can instruct an object to release each of its advisory connections prior to closing down.

The enumerator to which you get access through <b>IOleObject::EnumAdvise</b> enumerates items of type <a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a>. Upon receiving the pointer, the container can then loop through <b>STATDATA</b> and call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a> for each enumerated connection.

The usual way to implement this function is to delegate the call to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> interface. Only the <b>pAdvise</b> and <b>dwConnection</b> members of <a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a> are relevant for <b>IOleObject::EnumAdvise</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a>