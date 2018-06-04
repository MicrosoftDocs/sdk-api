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

# IOleDocumentView::CloseView


## -description


Instructs a document view to close itself and release its <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> pointer.


## -parameters




### -param dwReserved [in]

This parameter is reserved and cannot be <b>NULL</b>.


## -returns



This method returns S_OK on success.




## -remarks



When a separate window is no longer needed, the container calls <b>IOleDocumentView::CloseView</b>, whereupon the view releases its site pointer to the separate window and destroys the window. Unlike the normal in-place deactivation sequence for active documents, a document view continues to hold the <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> pointer. This pointer is released only when the view's container calls <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">SetInPlaceSite</a>, with <i>pIPSite</i> set to <b>NULL</b>, or calls <b>IOleDocumentView::CloseView</b>.

When a user closes a view's separate window, the view should not shut itself down. Instead, it should call <a href="https://msdn.microsoft.com/e5744911-1ea6-4482-988d-8def16229f4c">IOleInPlaceSite::OnInPlaceActivate</a>. The view site then decides whether to call <a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a> with <b>FALSE</b> immediately or later. In this way, a document view displayed in a separate window remains available for activation in the container's own window.

The container must call this method before it deletes the view, that is, releases its last reference to the view. In general, implementation of this method will call <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a> with <b>FALSE</b> to hide the view if it is not already hidden, then call <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">SetInPlaceSite</a> with <b>NULL</b> to deactivate itself and release the view site pointer.

Because <b>IOleDocumentView::CloseView</b> is called when a container is going to completely shut down a view, this method must be implemented and has no reason to fail.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>



<a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a>
 

 

