---
UID: NN:objidl.IAdviseSink
title: IAdviseSink (objidl.h)
description: Enables containers and other objects to receive notifications of data changes, view changes, and compound-document changes occurring in objects of interest.
helpviewer_keywords: ["IAdviseSink","IAdviseSink interface [COM]","IAdviseSink interface [COM]","described","_ole_iadvisesink","com.iadvisesink","objidl/IAdviseSink"]
old-location: com\iadvisesink.htm
tech.root: com
ms.assetid: bc9f217a-75bd-4155-9d00-df44b00cf0e5
ms.date: 12/05/2018
ms.keywords: IAdviseSink, IAdviseSink interface [COM], IAdviseSink interface [COM],described, _ole_iadvisesink, com.iadvisesink, objidl/IAdviseSink
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IAdviseSink
 - objidl/IAdviseSink
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
 - IAdviseSink
---

# IAdviseSink interface


## -description

Enables containers and other objects to receive notifications of data changes, view changes, and compound-document changes occurring in objects of interest. Container applications, for example, require such notifications to keep cached presentations of their linked and embedded objects up-to-date. Calls to <b>IAdviseSink</b> methods are asynchronous, so the call is sent and then the next instruction is executed without waiting for the call's return.

For an advisory connection to exist, the object that is to receive notifications must implement <b>IAdviseSink</b>, and the objects in which it is interested must implement <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a> and <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>. In-process objects and handlers may also implement <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a>. Objects implementing <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> must support all reasonable advisory methods. To simplify advisory notifications, OLE supplies implementations of the <a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a> and <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>, which keep track of advisory connections and send notifications to the proper sinks through pointers to their <b>IAdviseSink</b> interfaces. <a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a> (and its advisory methods) is implemented in the default handler.

As shown in the following table, an object that has implemented an advise sink registers its interest in receiving certain types of notifications by calling the appropriate method.
<table>
<tr>
<th>Call This Method</th>
<th> To Register for These Notifications</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>
</td>
<td>When a document is saved, closed, or renamed.
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>
</td>
<td>When a document's data changes.
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a>
</td>
<td>When a document's presentation changes.
</td>
</tr>
</table> 

When an event occurs that applies to a registered notification type, the object application calls the appropriate <b>IAdviseSink</b> method. For example, when an embedded object closes, it calls the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onclose">IAdviseSink::OnClose</a> method to notify its container. These notifications are asynchronous, occurring after the events that trigger them.

## -inheritance

The <b>IAdviseSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAdviseSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink2">IAdviseSink2</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iadvisesinkex">IAdviseSinkEx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a>
