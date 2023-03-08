---
UID: NF:objidl.IAdviseSink.OnDataChange
title: IAdviseSink::OnDataChange (objidl.h)
description: Called by the server to notify a data object's currently registered advise sinks that data in the object has changed.
helpviewer_keywords: ["IAdviseSink interface [COM]","OnDataChange method","IAdviseSink.OnDataChange","IAdviseSink::OnDataChange","OnDataChange","OnDataChange method [COM]","OnDataChange method [COM]","IAdviseSink interface","_ole_iadvisesink_ondatachange","com.iadvisesink_ondatachange","objidl/IAdviseSink::OnDataChange"]
old-location: com\iadvisesink_ondatachange.htm
tech.root: com
ms.assetid: 834a5328-3a1f-4edb-aad0-be8ab87acb04
ms.date: 12/05/2018
ms.keywords: IAdviseSink interface [COM],OnDataChange method, IAdviseSink.OnDataChange, IAdviseSink::OnDataChange, OnDataChange, OnDataChange method [COM], OnDataChange method [COM],IAdviseSink interface, _ole_iadvisesink_ondatachange, com.iadvisesink_ondatachange, objidl/IAdviseSink::OnDataChange
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
 - IAdviseSink::OnDataChange
 - objidl/IAdviseSink::OnDataChange
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
 - IAdviseSink.OnDataChange
---

# IAdviseSink::OnDataChange


## -description

Called by the server to notify a data object's currently registered advise sinks that data in the object has changed.

## -parameters

### -param pFormatetc [in]

A pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure, which describes the format, target device, rendering, and storage information of the calling data object.

### -param pStgmed [in]

A pointer to a <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure, which defines the storage medium (global memory, disk file, storage object, stream object, GDI object, or undefined) and ownership of that medium for the calling data object.

## -remarks

Object handlers and containers of link objects implement <b>IAdviseSink::OnDataChange</b> to take appropriate steps when notified that data in the object has changed. They also must call <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> to set up advisory connections with the objects in whose data they are interested.

Containers that take advantage of OLE's caching support do not need to register for data-change notifications, because the information necessary to update the container's presentation of the object, including any changes in its data, are maintained in the object's cache.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you implement <b>IAdviseSink::OnDataChange</b> for a container, remember that this method is asynchronous and that making synchronous calls within asynchronous methods is not valid. Therefore, you cannot call <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> to obtain the data you need to update your object. Instead, you either post an internal message, or invalidate the rectangle for the changed data by calling <a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a> and waiting for a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message, at which point you are free to get the data and update the object.

The data itself, which is valid only for the duration of the call, is passed using the storage medium pointed to by <i>pStgmed</i>. Since the caller owns the medium, the advise sink should not free it. Also, if <i>pStgmed</i> points to an <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> or <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface, the sink must not increment the reference count.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>