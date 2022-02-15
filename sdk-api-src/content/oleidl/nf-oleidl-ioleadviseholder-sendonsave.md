---
UID: NF:oleidl.IOleAdviseHolder.SendOnSave
title: IOleAdviseHolder::SendOnSave (oleidl.h)
description: Sends notification to all advisory sinks currently registered with the advise holder that the object has been saved.
helpviewer_keywords: ["IOleAdviseHolder interface [COM]","SendOnSave method","IOleAdviseHolder.SendOnSave","IOleAdviseHolder::SendOnSave","SendOnSave","SendOnSave method [COM]","SendOnSave method [COM]","IOleAdviseHolder interface","_ole_ioleadviseholder_sendonsave","com.ioleadviseholder_sendonsave","oleidl/IOleAdviseHolder::SendOnSave"]
old-location: com\ioleadviseholder_sendonsave.htm
tech.root: com
ms.assetid: b64ceaf7-45ba-4a66-a5cf-aec352472d3d
ms.date: 12/05/2018
ms.keywords: IOleAdviseHolder interface [COM],SendOnSave method, IOleAdviseHolder.SendOnSave, IOleAdviseHolder::SendOnSave, SendOnSave, SendOnSave method [COM], SendOnSave method [COM],IOleAdviseHolder interface, _ole_ioleadviseholder_sendonsave, com.ioleadviseholder_sendonsave, oleidl/IOleAdviseHolder::SendOnSave
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
 - IOleAdviseHolder::SendOnSave
 - oleidl/IOleAdviseHolder::SendOnSave
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
 - IOleAdviseHolder.SendOnSave
---

# IOleAdviseHolder::SendOnSave


## -description

Sends notification to all advisory sinks currently registered with the advise holder that the object has been saved.



## -returns

This method returns S_OK if advise sinks were sent <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onsave">IAdviseSink::OnSave</a> notifications.

## -remarks

<b>SendOnSave</b> calls <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onsave">IAdviseSink::OnSave</a> to advise the calling object (client), which must have already established an advisory connection, that the object has been saved. If you are using the OLE advise holder (having obtained a pointer through a call to <a href="/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>), you can call <b>SendOnSave</b> whenever you save the object the advise holder is associated with.

To take the object from the running state to the loaded state, the client calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>. Within that implementation, if the user wants to save the object to persistent storage, the object calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-saveobject">IOleClientSite::SaveObject</a>, followed by the call to <b>SendOnSave</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onsave">IAdviseSink::OnSave</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>
