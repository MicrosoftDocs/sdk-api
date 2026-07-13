---
UID: NN:objidl.IInternalUnknown
title: IInternalUnknown (objidl.h)
description: The IInternalUnknown interface (objidl.h) is used exclusively in lightweight client-side handlers that require access to the internal interfaces on the proxy. 
helpviewer_keywords: ["IInternalUnknown","IInternalUnknown interface [COM]","IInternalUnknown interface [COM]","described","_com_iinternalunknown","com.iinternalunknown","objidlbase/IInternalUnknown"]
old-location: com\iinternalunknown.htm
tech.root: com
ms.assetid: d2f4c8bc-80b9-4ba0-9f30-f0864144902b
ms.date: 08/15/2022
ms.keywords: IInternalUnknown, IInternalUnknown interface [COM], IInternalUnknown interface [COM],described, _com_iinternalunknown, com.iinternalunknown, objidlbase/IInternalUnknown
req.header: objidl.h
req.include-header: ObjIdl.h
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
 - IInternalUnknown
 - objidl/IInternalUnknown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IInternalUnknown
---

# IInternalUnknown interface


## -description

Used exclusively in lightweight client-side handlers that require access to some of the internal interfaces on the proxy.

## -inheritance

The <b>IInternalUnknown</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInternalUnknown</b> also has these types of members:

## -remarks

Handlers that need access to some of the internal interfaces on the proxy manager have to go through the <b>IInternalUnknown</b> interface. This prevents the handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate. These interfaces include <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> and <a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a>. If the handler wants to expose <b>IClientSecurity</b> or <b>IMultiQI</b>, the handler should implement these interfaces itself and delegate to the proxy manager's implementation of these interfaces when appropriate.

For the <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> interface, if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.



For the <a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a> interface, the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to fill in the rest of the interfaces.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a>



<a href="/windows/desktop/com/the-lightweight-client-side-handler">Lightweight Client-Side Handler</a>
