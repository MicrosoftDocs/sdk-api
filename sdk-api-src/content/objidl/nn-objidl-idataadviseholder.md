---
UID: NN:objidl.IDataAdviseHolder
title: IDataAdviseHolder (objidl.h)
description: Creates and manages advisory connections between a data object and one or more advise sinks.
helpviewer_keywords: ["IDataAdviseHolder","IDataAdviseHolder interface [COM]","IDataAdviseHolder interface [COM]","described","_ole_idataadviseholder","com.idataadviseholder","objidl/IDataAdviseHolder"]
old-location: com\idataadviseholder.htm
tech.root: com
ms.assetid: 740a6366-6ab1-4a20-82df-1efdd62211eb
ms.date: 12/05/2018
ms.keywords: IDataAdviseHolder, IDataAdviseHolder interface [COM], IDataAdviseHolder interface [COM],described, _ole_idataadviseholder, com.idataadviseholder, objidl/IDataAdviseHolder
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
 - IDataAdviseHolder
 - objidl/IDataAdviseHolder
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
 - IDataAdviseHolder
---

# IDataAdviseHolder interface


## -description

Creates and manages advisory connections between a data object and one or more advise sinks. Its methods are intended to be used to implement the advisory methods of <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>. <b>IDataAdviseHolder</b> is implemented on an advise holder object. Its methods establish and delete data advisory connections and send notification of change in data from a data object to an object that requires this notification, such as an OLE container, which must contain an advise sink.

Advise sinks are objects that require notification of change in the data the object contains and implement the <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface. Advise sinks are also usually associated with OLE compound document containers.

## -inheritance

The <b>IDataAdviseHolder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataAdviseHolder</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>
