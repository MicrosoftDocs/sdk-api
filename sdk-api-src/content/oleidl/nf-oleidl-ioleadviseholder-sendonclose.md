---
UID: NF:oleidl.IOleAdviseHolder.SendOnClose
title: IOleAdviseHolder::SendOnClose (oleidl.h)
description: Sends notification to all advisory sinks currently registered with the advise holder that the object has closed.
helpviewer_keywords: ["IOleAdviseHolder interface [COM]","SendOnClose method","IOleAdviseHolder.SendOnClose","IOleAdviseHolder::SendOnClose","SendOnClose","SendOnClose method [COM]","SendOnClose method [COM]","IOleAdviseHolder interface","_ole_ioleadviseholder_sendonclose","com.ioleadviseholder_sendonclose","oleidl/IOleAdviseHolder::SendOnClose"]
old-location: com\ioleadviseholder_sendonclose.htm
tech.root: com
ms.assetid: f4efa947-d357-432c-9585-b00b19551ad6
ms.date: 12/05/2018
ms.keywords: IOleAdviseHolder interface [COM],SendOnClose method, IOleAdviseHolder.SendOnClose, IOleAdviseHolder::SendOnClose, SendOnClose, SendOnClose method [COM], SendOnClose method [COM],IOleAdviseHolder interface, _ole_ioleadviseholder_sendonclose, com.ioleadviseholder_sendonclose, oleidl/IOleAdviseHolder::SendOnClose
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
 - IOleAdviseHolder::SendOnClose
 - oleidl/IOleAdviseHolder::SendOnClose
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
 - IOleAdviseHolder.SendOnClose
---

# IOleAdviseHolder::SendOnClose


## -description

Sends notification to all advisory sinks currently registered with the advise holder that the object has closed.



## -returns

This method returns S_OK if advise sinks were notified of the close operation through a call to the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a> method.

## -remarks

<b>SendOnClose</b> must call <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a> on all advise sinks that have a valid advisory connection with the object, whenever the object goes from the running state to the loaded state. This occurs through a call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>, so you can call <b>SendOnClose</b> when you determine that a Close operation has been successful.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>
