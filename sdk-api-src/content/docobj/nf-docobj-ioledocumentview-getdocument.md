---
UID: NF:docobj.IOleDocumentView.GetDocument
title: IOleDocumentView::GetDocument method
author: windows-driver-content
description: Obtains the IUnknown interface pointer on the document object that owns this view.
old-location: com\ioledocumentview_getdocument.htm
old-project: com
ms.assetid: 46174e4f-c943-4e70-af68-79363962cdee
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetDocument method [COM], GetDocument method [COM], IOleDocumentView interface, GetDocument,IOleDocumentView.GetDocument, IOleDocumentView, IOleDocumentView interface [COM], GetDocument method, IOleDocumentView::GetDocument, _ole_ioledocumentview_getdocument, com.ioledocumentview_getdocument, docobj/IOleDocumentView::GetDocument
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DOCMISC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DocObj.h
api_name:
-	IOleDocumentView.GetDocument
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::GetDocument method


## -description


Obtains the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer on the document object that owns this view.


## -parameters




### -param ppunk [out]

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer that receives a pointer to the document object that owns this view.


## -returns



This method returns S_OK on success. S_OK is the only valid return value for this method.




## -remarks



The caller is responsible for incrementing the reference count on the interface pointer obtained by this method. The caller must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on this pointer when it is no longer needed.

Because a view object must always be contained or aggregated in a document object, this method will always succeed. Before returning, this method should call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on the pointer stored in <i>ppunk</i>.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

