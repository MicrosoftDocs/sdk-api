---
UID: NF:objidl.IAdviseSink.OnDataChange
title: IAdviseSink::OnDataChange
author: windows-sdk-content
description: Called by the server to notify a data object's currently registered advise sinks that data in the object has changed.
old-location: com\iadvisesink_ondatachange.htm
tech.root: com
ms.assetid: 834a5328-3a1f-4edb-aad0-be8ab87acb04
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAdviseSink interface [COM],OnDataChange method, IAdviseSink.OnDataChange, IAdviseSink::OnDataChange, OnDataChange, OnDataChange method [COM], OnDataChange method [COM],IAdviseSink interface, _ole_iadvisesink_ondatachange, com.iadvisesink_ondatachange, objidl/IAdviseSink::OnDataChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAdviseSink.OnDataChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAdviseSink::OnDataChange


## -description


Called by the server to notify a data object's currently registered advise sinks that data in the object has changed.


## -parameters




### -param pFormatetc [in]

A pointer to a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure, which describes the format, target device, rendering, and storage information of the calling data object.


### -param pStgmed [in]

A pointer to a <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> structure, which defines the storage medium (global memory, disk file, storage object, stream object, GDI object, or undefined) and ownership of that medium for the calling data object.


## -returns



This method does not return a value.




## -remarks



Object handlers and containers of link objects implement <b>IAdviseSink::OnDataChange</b> to take appropriate steps when notified that data in the object has changed. They also must call <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> to set up advisory connections with the objects in whose data they are interested.

Containers that take advantage of OLE's caching support do not need to register for data-change notifications, because the information necessary to update the container's presentation of the object, including any changes in its data, are maintained in the object's cache.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you implement <b>IAdviseSink::OnDataChange</b> for a container, remember that this method is asynchronous and that making synchronous calls within asynchronous methods is not valid. Therefore, you cannot call <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> to obtain the data you need to update your object. Instead, you either post an internal message, or invalidate the rectangle for the changed data by calling <a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a> and waiting for a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message, at which point you are free to get the data and update the object.

The data itself, which is valid only for the duration of the call, is passed using the storage medium pointed to by <i>pStgmed</i>. Since the caller owns the medium, the advise sink should not free it. Also, if <i>pStgmed</i> points to an <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> or <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface, the sink must not increment the reference count.




## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>
 

 

