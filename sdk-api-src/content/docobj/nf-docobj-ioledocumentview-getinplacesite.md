---
UID: NF:docobj.IOleDocumentView.GetInPlaceSite
title: IOleDocumentView::GetInPlaceSite
author: windows-sdk-content
description: Retrieves the view site associated with this view object.
old-location: com\ioledocumentview_getinplacesite.htm
tech.root: com
ms.assetid: d48cd54c-11b3-4acd-a13a-75a612f1761a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetInPlaceSite, GetInPlaceSite method [COM], GetInPlaceSite method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],GetInPlaceSite method, IOleDocumentView.GetInPlaceSite, IOleDocumentView::GetInPlaceSite, _ole_ioledocumentview_getinplacesite, com.ioledocumentview_getinplacesite, docobj/IOleDocumentView::GetInPlaceSite
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleDocumentView::GetInPlaceSite


## -description


Retrieves the view site associated with this view object.


## -parameters




### -param ppIPSite [out]

A pointer to an <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> pointer variable that receives the interface pointer to the document's view site.


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



<b>IOleDocumentView::GetInPlaceSite</b> obtains the most recent <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> pointer passed by <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>, or <b>NULL</b> if <b>IOleDocumentView::SetInPlaceSite</b> has not yet been called. If this pointer is not <b>NULL</b>, this method will call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on the pointer. The caller is responsible for releasing it. A document view must implement this method completely; E_NOTIMPL is not an acceptable return value.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 

