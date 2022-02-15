---
UID: NF:objidl.IAdviseSink.OnClose
title: IAdviseSink::OnClose (objidl.h)
description: Called by the server to notify all registered advisory sinks that the object has changed from the running to the loaded state.
helpviewer_keywords: ["IAdviseSink interface [COM]","OnClose method","IAdviseSink.OnClose","IAdviseSink::OnClose","OnClose","OnClose method [COM]","OnClose method [COM]","IAdviseSink interface","_ole_iadvisesink_onclose","com.iadvisesink_onclose","objidl/IAdviseSink::OnClose"]
old-location: com\iadvisesink_onclose.htm
tech.root: com
ms.assetid: a695c623-4a4e-4f3d-9f12-ee198c0761a9
ms.date: 12/05/2018
ms.keywords: IAdviseSink interface [COM],OnClose method, IAdviseSink.OnClose, IAdviseSink::OnClose, OnClose, OnClose method [COM], OnClose method [COM],IAdviseSink interface, _ole_iadvisesink_onclose, com.iadvisesink_onclose, objidl/IAdviseSink::OnClose
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IAdviseSink::OnClose
 - objidl/IAdviseSink::OnClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IAdviseSink.OnClose
---

# IAdviseSink::OnClose


## -description

Called by the server to notify all registered advisory sinks that the object has changed from the running to the loaded state.



## -remarks

The <b>OnClose</b> notification indicates that an object is making the transition from the running to the loaded state, so its container can take appropriate measures to ensure an orderly shutdown. For example, an object handler must release its pointer to the object.

If the object that is closing is the last open object supported by its OLE server application, the application can also shut down.

In the case of a link object, the notification that the object is closing should always be interpreted to mean that the connection to the link source has broken.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>
