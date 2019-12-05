---
UID: NN:objidl.IDataAdviseHolder
title: IDataAdviseHolder (objidl.h)
description: Creates and manages advisory connections between a data object and one or more advise sinks.
old-location: com\idataadviseholder.htm
tech.root: com
ms.assetid: 740a6366-6ab1-4a20-82df-1efdd62211eb
ms.date: 12/05/2018
ms.keywords: IDataAdviseHolder, IDataAdviseHolder interface [COM], IDataAdviseHolder interface [COM],described, _ole_idataadviseholder, com.idataadviseholder, objidl/IDataAdviseHolder
ms.topic: interface
f1_keywords:
- objidl/IDataAdviseHolder
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ObjIdl.h
api_name:
- IDataAdviseHolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataAdviseHolder interface


## -description


Creates and manages advisory connections between a data object and one or more advise sinks. Its methods are intended to be used to implement the advisory methods of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>. <b>IDataAdviseHolder</b> is implemented on an advise holder object. Its methods establish and delete data advisory connections and send notification of change in data from a data object to an object that requires this notification, such as an OLE container, which must contain an advise sink.

Advise sinks are objects that require notification of change in the data the object contains and implement the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface. Advise sinks are also usually associated with OLE compound document containers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataAdviseHolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataAdviseHolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataAdviseHolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">Advise</a>
</td>
<td align="left" width="63%">
Creates a connection between an advise sink and a data object so the advise sink can receive notification of change in the data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-enumadvise">EnumAdvise</a>
</td>
<td align="left" width="63%">
Returns an object that can be used to enumerate the current advisory connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-sendondatachange">SendOnDataChange</a>
</td>
<td align="left" width="63%">
Sends a change notification back to each advise sink that is currently being managed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Destroys a notification connection previously set up with the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">Advise</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>
 

 

