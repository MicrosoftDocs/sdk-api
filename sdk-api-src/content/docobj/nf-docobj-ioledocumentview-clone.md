---
UID: NF:docobj.IOleDocumentView.Clone
title: IOleDocumentView::Clone
author: windows-sdk-content
description: Creates a duplicate view object with an internal state identical to that of the current view.
old-location: com\ioledocumentview_clone.htm
tech.root: com
ms.assetid: d8acc469-26f6-4f1b-94a5-4839aa235a1d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],Clone method, IOleDocumentView.Clone, IOleDocumentView::Clone, _ole_ioledocumentview_clone, com.ioledocumentview_clone, docobj/IOleDocumentView::Clone
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
 - IOleDocumentView.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleDocumentView::Clone


## -description


Creates a duplicate view object with an internal state identical to that of the current view.


## -parameters




### -param pIPSiteNew [in]

A pointer to a <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a> interface that represents the view site in which the new view object will be activated. On receiving this pointer, the view being cloned should pass it to the new view's <a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a> method. This pointer can be <b>NULL</b>, in which case the caller is responsible for calling <b>IOleDocumentView::SetInPlaceSite</b> on the new view directly.


### -param ppViewNew [out]

A pointer to an <a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a> pointer variable that receives the interface pointer to the new view object. The caller is responsible for releasing <i>ppViewNew</i> when it is no longer needed.


## -returns



This method returns S_OK on success. Other possible return values include the following.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>ppViewNew</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The view object does not implement this interface.

</td>
</tr>
</table>
 




## -remarks



This method is useful for creating a new view with a different viewport and view site but with the same view context as the view being cloned. Typically, containers hosting an MDI application will call this method to provide "Window/New window" capability.




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/88de47c2-979b-4595-8a2f-d4ed1a3a7b6c">IOleDocumentView::SetInPlaceSite</a>
 

 

