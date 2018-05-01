---
UID: NF:docobj.IOleDocumentView.ApplyViewState
title: IOleDocumentView::ApplyViewState method
author: windows-driver-content
description: Initializes a view with view state previously saved in call to IOleDocumentView::SaveViewState.
old-location: com\ioledocumentview_applyviewstate.htm
old-project: com
ms.assetid: f78526b4-977a-4dde-8a2f-7ae0a1c5c7f9
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: ApplyViewState method [COM], ApplyViewState method [COM], IOleDocumentView interface, ApplyViewState,IOleDocumentView.ApplyViewState, IOleDocumentView, IOleDocumentView interface [COM], ApplyViewState method, IOleDocumentView::ApplyViewState, _ole_ioledocumentview_applyviewstate, com.ioledocumentview_applyviewstate, docobj/IOleDocumentView::ApplyViewState
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
-	IOleDocumentView.ApplyViewState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::ApplyViewState method


## -description


Initializes a view with view state previously saved in call to <a href="https://msdn.microsoft.com/d270b441-d0d5-4dd5-995b-6ca5738747c5">IOleDocumentView::SaveViewState</a>.


## -parameters




### -param pstm [in]

A pointer to a stream containing data from which the view should initialize itself.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>pstm</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This view has no meaningful state to load. This error should be rare because most views will have at least some state information worth loading.

</td>
</tr>
</table>
 




## -remarks



Typically, this function is called after an existing view has been created in the container but before that view has been displayed. It is the responsibility of the view to validate the data in the view stream; the container does not attempt to interpret the view's state data.




## -see-also




<a href="https://msdn.microsoft.com/709d7ff4-d32d-405f-8839-b05df49ef751">IOleDocument::CreateView</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/d270b441-d0d5-4dd5-995b-6ca5738747c5">IOleDocumentView::SaveViewState</a>
 

 

