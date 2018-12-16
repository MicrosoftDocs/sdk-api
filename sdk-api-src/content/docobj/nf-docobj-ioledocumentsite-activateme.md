---
UID: NF:docobj.IOleDocumentSite.ActivateMe
title: IOleDocumentSite::ActivateMe
author: windows-sdk-content
description: Asks a document site to activate the document making the call as a document object rather than an in-place-active object and, optionally, specifies which view of the object document to activate.
old-location: com\ioledocumentsite_activateme.htm
tech.root: com
ms.assetid: 4e4a746d-460a-478e-9ca5-be5f63b03d17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ActivateMe, ActivateMe method [COM], ActivateMe method [COM],IOleDocumentSite interface, IOleDocumentSite interface [COM],ActivateMe method, IOleDocumentSite.ActivateMe, IOleDocumentSite::ActivateMe, _ole_ioledocumentsite_activateme, com.ioledocumentsite_activateme, docobj/IOleDocumentSite::ActivateMe
ms.topic: method
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
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
 - DocObj.h
api_name:
 - IOleDocumentSite.ActivateMe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleDocumentSite::ActivateMe


## -description


Asks a document site to activate the document making the call as a document object rather than an in-place-active object and, optionally, specifies which view of the object document to activate.


## -parameters




### -param pViewToActivate [in]

A pointer to an <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> interface pointer that represents the document view to be used in activating the document object. This parameter can be <b>NULL</b>, in which case the container should call <a href="https://msdn.microsoft.com/709d7ff4-d32d-405f-8839-b05df49ef751">IOleDocument::CreateView</a> to obtain a document view pointer.


## -returns



This method returns S_OK on success.




## -remarks



When a container calls <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a> to activate a document, a document object bypasses the usual in-place activation sequence by calling <b>IOleDocumentSite::ActivateMe</b>.

When calling <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a> on a document object, the most appropriate activation verb is usually OLEIVERB_SHOW. Other allowable verbs include OLEIVERB_PRIMARY and OLEIVERB_UIACTIVATE. OLEIVERB_OPEN is discouraged because it means opening an embedded object in a separate window, which is contrary to the intent of document object activation.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Only document objects should call this method. A normal in-place active document should respond to a container's call to <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a> by calling <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>.

A document object should initiate its activation by calling <b>IOleDocumentSite::ActivateMe</b>. If the container does not implement <a href="https://msdn.microsoft.com/cac435c9-caee-4751-9ad8-df48b6d4c7e0">IOleDocumentSite</a>, then the document should default to the normal in-place activation sequence.

A document object that supports more than one view of its data can specify which view to activate by passing a pointer to that view's <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> interface in <i>pViewToActivate</i>.

However the <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> pointer is obtained, the container should release the pointer when it is no longer needed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This function must be completely implemented in a document object container; E_NOTIMPL is not an acceptable return value.

If a document object passes an <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> pointer in <i>pViewToActivate</i>, the container's implementation of <b>IOleDocumentSite::ActivateMe</b> should call <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a> and pass a pointer to its <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> interface back to the view object. If the container is holding onto the <b>IOleDocumentView</b> pointer, which will normally be the case, it should follow the call to <b>IOleDocumentView::SetInPlaceSite</b> with a call to <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a>.



If <i>pViewToActivate</i> is <b>NULL</b>, the container can obtain a pointer to a document view by querying the document for <a href="https://msdn.microsoft.com/7a15d6ef-900c-4a0b-8b85-60dc66ca03a3">IOleDocument</a>, then calling <a href="https://msdn.microsoft.com/709d7ff4-d32d-405f-8839-b05df49ef751">IOleDocument::CreateView</a> and passing its <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> pointer.




## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>



<a href="https://msdn.microsoft.com/709d7ff4-d32d-405f-8839-b05df49ef751">IOleDocument::CreateView</a>



<a href="https://msdn.microsoft.com/cac435c9-caee-4751-9ad8-df48b6d4c7e0">IOleDocumentSite</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>



<a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a>
 

 

