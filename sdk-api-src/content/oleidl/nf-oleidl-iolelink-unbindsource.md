---
UID: NF:oleidl.IOleLink.UnbindSource
title: IOleLink::UnbindSource (oleidl.h)
description: Breaks the connection between a linked object and its link source.
helpviewer_keywords: ["IOleLink interface [COM]","UnbindSource method","IOleLink.UnbindSource","IOleLink::UnbindSource","UnbindSource","UnbindSource method [COM]","UnbindSource method [COM]","IOleLink interface","_ole_iolelink_unbindsource","com.iolelink_unbindsource","oleidl/IOleLink::UnbindSource"]
old-location: com\iolelink_unbindsource.htm
tech.root: com
ms.assetid: 3a678944-b4ba-47d8-9a89-470762efc6f9
ms.date: 12/05/2018
ms.keywords: IOleLink interface [COM],UnbindSource method, IOleLink.UnbindSource, IOleLink::UnbindSource, UnbindSource, UnbindSource method [COM], UnbindSource method [COM],IOleLink interface, _ole_iolelink_unbindsource, com.iolelink_unbindsource, oleidl/IOleLink::UnbindSource
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
 - IOleLink::UnbindSource
 - oleidl/IOleLink::UnbindSource
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
 - IOleLink.UnbindSource
---

# IOleLink::UnbindSource


## -description

Breaks the connection between a linked object and its link source.



## -returns

This method returns S_OK on success.

## -remarks

You typically do not call <b>UnbindSource</b> directly. When it's necessary to deactivate the connection to the link source, your container typically calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a> or <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>; the linked object's implementation of these methods calls <b>UnbindSource</b>. The linked object's <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a> implementation also calls <b>UnbindSource</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The linked object's implementation of <b>UnbindSource</b> does nothing if the link source is not currently bound. If the link source is bound, <b>UnbindSource</b> calls the link source's <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a> and <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dunadvise">IDataObject::DUnadvise</a> implementations to delete the advisory connections to the link source. The <b>UnbindSource</b> method also calls the compound document's <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">IOleContainer::LockContainer</a> implementation to unlock the containing compound document. This undoes the lock on the container and the advisory connections that were established in <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>. <b>UnbindSource</b> releases all the linked object's interface pointers to the link source.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dunadvise">IDataObject::DUnadvise</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">IOleLink::BindToSource</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a>
