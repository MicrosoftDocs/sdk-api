---
UID: NF:docobj.IOleDocumentView.GetDocument
title: IOleDocumentView::GetDocument (docobj.h)
description: Obtains the IUnknown interface pointer on the document object that owns this view.
old-location: com\ioledocumentview_getdocument.htm
tech.root: com
ms.assetid: 46174e4f-c943-4e70-af68-79363962cdee
ms.date: 12/05/2018
ms.keywords: GetDocument, GetDocument method [COM], GetDocument method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],GetDocument method, IOleDocumentView.GetDocument, IOleDocumentView::GetDocument, _ole_ioledocumentview_getdocument, com.ioledocumentview_getdocument, docobj/IOleDocumentView::GetDocument
f1_keywords:
- docobj/IOleDocumentView.GetDocument
dev_langs:
- c++
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
- IOleDocumentView.GetDocument
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleDocumentView::GetDocument


## -description


Obtains the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer on the document object that owns this view.


## -parameters




### -param ppunk [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer that receives a pointer to the document object that owns this view.


## -returns



This method returns S_OK on success. S_OK is the only valid return value for this method.




## -remarks



The caller is responsible for incrementing the reference count on the interface pointer obtained by this method. The caller must call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on this pointer when it is no longer needed.

Because a view object must always be contained or aggregated in a document object, this method will always succeed. Before returning, this method should call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the pointer stored in <i>ppunk</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

