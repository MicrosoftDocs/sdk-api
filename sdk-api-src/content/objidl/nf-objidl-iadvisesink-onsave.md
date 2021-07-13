---
UID: NF:objidl.IAdviseSink.OnSave
title: IAdviseSink::OnSave (objidl.h)
description: Called by the server to notify all registered advisory sinks that the object has been saved.
helpviewer_keywords: ["IAdviseSink interface [COM]","OnSave method","IAdviseSink.OnSave","IAdviseSink::OnSave","OnSave","OnSave method [COM]","OnSave method [COM]","IAdviseSink interface","_ole_iadvisesink_onsave","com.iadvisesink_onsave","objidl/IAdviseSink::OnSave"]
old-location: com\iadvisesink_onsave.htm
tech.root: com
ms.assetid: 26da5e16-5790-49c0-ba63-5feee49cd4c6
ms.date: 12/05/2018
ms.keywords: IAdviseSink interface [COM],OnSave method, IAdviseSink.OnSave, IAdviseSink::OnSave, OnSave, OnSave method [COM], OnSave method [COM],IAdviseSink interface, _ole_iadvisesink_onsave, com.iadvisesink_onsave, objidl/IAdviseSink::OnSave
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
 - IAdviseSink::OnSave
 - objidl/IAdviseSink::OnSave
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
 - IAdviseSink.OnSave
---

# IAdviseSink::OnSave


## -description

Called by the server to notify all registered advisory sinks that the object has been saved.



## -remarks

Object handlers and link objects normally implement <b>IAdviseSink::OnSave</b> to receive notifications of when an object is saved to disk, either to its original storage (through a <b>Save</b> operation) or to new storage (through a <b>Save As</b> operation). Object Handlers and link objects register to be notified when an object is saved for the purpose of updating their caches, but then only if the advise flag passed during registration specifies ADVFCACHE_ONSAVE. Object handlers and link objects forward these notifications to their containers.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>
