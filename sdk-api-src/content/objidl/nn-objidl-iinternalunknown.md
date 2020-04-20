---
UID: NN:objidl.IInternalUnknown
title: IInternalUnknown (objidl.h)
description: Used exclusively in lightweight client-side handlers that require access to some of the internal interfaces on the proxy.helpviewer_keywords: ["IInternalUnknown","IInternalUnknown interface [COM]","IInternalUnknown interface [COM]","described","_com_iinternalunknown","com.iinternalunknown","objidlbase/IInternalUnknown"]
old-location: com\iinternalunknown.htm
tech.root: com
ms.assetid: d2f4c8bc-80b9-4ba0-9f30-f0864144902b
ms.date: 12/05/2018
ms.keywords: IInternalUnknown, IInternalUnknown interface [COM], IInternalUnknown interface [COM],described, _com_iinternalunknown, com.iinternalunknown, objidlbase/IInternalUnknown
f1_keywords:
- objidl/IInternalUnknown
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IInternalUnknown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInternalUnknown interface


## -description


Used exclusively in lightweight client-side handlers that require access to some of the internal interfaces on the proxy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInternalUnknown</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInternalUnknown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInternalUnknown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iinternalunknown-queryinternalinterface">QueryInternalInterface</a>
</td>
<td align="left" width="63%">
Retrieves pointers to the supported internal interfaces on an object.

</td>
</tr>
</table> 


## -remarks



Handlers that need access to some of the internal interfaces on the proxy manager have to go through the <b>IInternalUnknown</b> interface. This prevents the handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate. These interfaces include <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> and <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a>. If the handler wants to expose <b>IClientSecurity</b> or <b>IMultiQI</b>, the handler should implement these interfaces itself and delegate to the proxy manager's implementation of these interfaces when appropriate.

For the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a> interface, if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.



For the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a> interface, the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to fill in the rest of the interfaces.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a>



<a href="https://docs.microsoft.com/windows/desktop/com/the-lightweight-client-side-handler">Lightweight Client-Side Handler</a>
 

 

