---
UID: NF:docobj.IOleDocumentView.GetInPlaceSite
title: IOleDocumentView::GetInPlaceSite (docobj.h)
author: windows-sdk-content
description: Retrieves the view site associated with this view object.
old-location: com\ioledocumentview_getinplacesite.htm
tech.root: com
ms.assetid: d48cd54c-11b3-4acd-a13a-75a612f1761a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInPlaceSite, GetInPlaceSite method [COM], GetInPlaceSite method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],GetInPlaceSite method, IOleDocumentView.GetInPlaceSite, IOleDocumentView::GetInPlaceSite, _ole_ioledocumentview_getinplacesite, com.ioledocumentview_getinplacesite, docobj/IOleDocumentView::GetInPlaceSite
ms.topic: method
f1_keywords: 
 - "docobj/IOleDocumentView.GetInPlaceSite"
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
 - IOleDocumentView.GetInPlaceSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleDocumentView::GetInPlaceSite


## -description


Retrieves the view site associated with this view object.


## -parameters




### -param ppIPSite [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer variable that receives the interface pointer to the document's view site.


## -returns



This method returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 




## -remarks



<b>IOleDocumentView::GetInPlaceSite</b> obtains the most recent <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a> pointer passed by <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>, or <b>NULL</b> if <b>IOleDocumentView::SetInPlaceSite</b> has not yet been called. If this pointer is not <b>NULL</b>, this method will call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the pointer. The caller is responsible for releasing it. A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setinplacesite">IOleDocumentView::SetInPlaceSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
 

 

