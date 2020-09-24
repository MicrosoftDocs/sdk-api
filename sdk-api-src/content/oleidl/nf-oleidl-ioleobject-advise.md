---
UID: NF:oleidl.IOleObject.Advise
title: IOleObject::Advise (oleidl.h)
description: Establishes an advisory connection between a compound document object and the calling object's advise sink, through which the calling object receives notification when the compound document object is renamed, saved, or closed.
helpviewer_keywords: ["Advise","Advise method [COM]","Advise method [COM]","IOleObject interface","IOleObject interface [COM]","Advise method","IOleObject.Advise","IOleObject::Advise","_ole_ioleobject_advise","com.ioleobject_advise","oleidl/IOleObject::Advise"]
old-location: com\ioleobject_advise.htm
tech.root: com
ms.assetid: 6a68c9e9-6e06-4def-89a5-18e184e76a26
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [COM], Advise method [COM],IOleObject interface, IOleObject interface [COM],Advise method, IOleObject.Advise, IOleObject::Advise, _ole_ioleobject_advise, com.ioleobject_advise, oleidl/IOleObject::Advise
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
 - IOleObject::Advise
 - oleidl/IOleObject::Advise
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
 - IOleObject.Advise
---

# IOleObject::Advise


## -description

Establishes an advisory connection between a compound document object and the calling object's advise sink, through which the calling object receives notification when the compound document object is renamed, saved, or closed.

## -parameters

### -param pAdvSink [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface on the advise sink of the calling object.

### -param pdwConnection [out]

Pointer to a token that can be passed to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a> to delete the advisory connection.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

The <b>IOleObject::Advise</b> method sets up an advisory connection between an object and its container, through which the object informs the container's advise sink of close, save, rename, and link-source change events in the object. A container calls this method, normally as part of initializing an object, to register its advisory sink with the object. In return, the object sends the container compound-document notifications by calling <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> or <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink2">IAdviseSink2</a>.

If container and object successfully establish an advisory connection, the object receiving the call returns a nonzero value through <i>pdwConnection</i> to the container. If the attempt to establish an advisory connection fails, the object returns zero. To delete an advisory connection, the container calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a> and passes this nonzero token back to the object.

An object can delegate the job of managing and tracking advisory events to an OLE advise holder, to which you obtain a pointer by calling <a href="/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>. The returned <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> interface has three methods for sending advisory notifications, as well as <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-advise">IOleAdviseHolder::Advise</a>, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-unadvise">IOleAdviseHolder::Unadvise</a>, and <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">IOleAdviseHolder::EnumAdvise</a> methods that are identical to those for <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>. Calls to <b>IOleObject::Advise</b>, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a>, or <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise">IOleObject::EnumAdvise</a> are delegated to corresponding methods in the advise holder.

To destroy the advise holder, simply call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> interface.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-advise">IOleAdviseHolder::Advise</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise">IOleObject::EnumAdvise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a>