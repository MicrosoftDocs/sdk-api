---
UID: NF:oleidl.IOleAdviseHolder.Advise
title: IOleAdviseHolder::Advise (oleidl.h)
description: Establishes an advisory connection between an OLE object and the calling object's advise sink. Through that sink, the calling object can receive notification when the OLE object is renamed, saved, or closed.
helpviewer_keywords: ["Advise","Advise method [COM]","Advise method [COM]","IOleAdviseHolder interface","IOleAdviseHolder interface [COM]","Advise method","IOleAdviseHolder.Advise","IOleAdviseHolder::Advise","_ole_ioleadviseholder_advise","com.ioleadviseholder_advise","oleidl/IOleAdviseHolder::Advise"]
old-location: com\ioleadviseholder_advise.htm
tech.root: com
ms.assetid: 60bbb555-7d01-49cb-b7b3-9dc905066f94
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [COM], Advise method [COM],IOleAdviseHolder interface, IOleAdviseHolder interface [COM],Advise method, IOleAdviseHolder.Advise, IOleAdviseHolder::Advise, _ole_ioleadviseholder_advise, com.ioleadviseholder_advise, oleidl/IOleAdviseHolder::Advise
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
 - IOleAdviseHolder::Advise
 - oleidl/IOleAdviseHolder::Advise
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
 - IOleAdviseHolder.Advise
---

# IOleAdviseHolder::Advise


## -description

Establishes an advisory connection between an OLE object and the calling object's advise sink. Through that sink, the calling object can receive notification when the OLE object is renamed, saved, or closed.

## -parameters

### -param pAdvise [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface on the advisory sink that should be informed of changes.

### -param pdwConnection [out]

A pointer to a token that can be passed to the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-unadvise">IOleAdviseHolder::Unadvise</a> method to delete the advisory connection. The calling object is responsible for calling both <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> and <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on this pointer.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface pointer is invalid.

</td>
</tr>
</table>

## -remarks

Containers, object handlers, and link objects all create advise sinks to receive notification of changes in compound-document objects of interest, such as embedded or linked objects. OLE objects of interest to these objects must implement the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface, which includes several advisory methods, including <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>. A call to this method must set up an advisory connection with any advise sink that calls it, and maintain each connection until it is closed. It must be able to handle more than one advisory connection at a time.

<b>IOleAdviseHolder::Advise</b> is intended to be used to simplify the implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>. You can get a pointer to the OLE implementation of IOleAdviseHolder by calling <a href="/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>, and then, to implement <b>IOleObject::Advise</b>, just delegate the call to <b>IOleAdviseHolder::Advise</b>. Other <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a> methods are intended to implement other <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> advisory methods.

If the attempt to establish an advisory connection is successful, the object receiving the call returns a nonzero value through <i>pdwConnection</i>. If the attempt fails, the object returns a zero. To delete an advisory connection, the object with the advise sink passes this nonzero token back to the object by calling <b>IOleAdviseHolder::Advise</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">IOleAdviseHolder::EnumAdvise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-unadvise">IOleAdviseHolder::Unadvise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>