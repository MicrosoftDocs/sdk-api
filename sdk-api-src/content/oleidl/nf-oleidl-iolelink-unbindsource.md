---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOleLink::UnbindSource


## -description


Breaks the connection between a linked object and its link source.


## -parameters






## -returns



This method returns S_OK on success.




## -remarks



You typically do not call <b>UnbindSource</b> directly. When it's necessary to deactivate the connection to the link source, your container typically calls <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a> or <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>; the linked object's implementation of these methods calls <b>UnbindSource</b>. The linked object's <a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a> implementation also calls <b>UnbindSource</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The linked object's implementation of <b>UnbindSource</b> does nothing if the link source is not currently bound. If the link source is bound, <b>UnbindSource</b> calls the link source's <a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a> and <a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a> implementations to delete the advisory connections to the link source. The <b>UnbindSource</b> method also calls the compound document's <a href="https://msdn.microsoft.com/31b9961a-29a2-48bf-9d39-d86718983682">IOleContainer::LockContainer</a> implementation to unlock the containing compound document. This undoes the lock on the container and the advisory connections that were established in <a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">IOleLink::BindToSource</a>. <b>UnbindSource</b> releases all the linked object's interface pointers to the link source.




## -see-also




<a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a>



<a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a>



<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>



<a href="https://msdn.microsoft.com/1fadd27d-cb2c-47fc-891a-16f82bdac0f6">IOleLink::BindToSource</a>



<a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>



<a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a>
 

 

