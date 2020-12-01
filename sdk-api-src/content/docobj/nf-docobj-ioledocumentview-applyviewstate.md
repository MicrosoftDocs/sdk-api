---
UID: NF:docobj.IOleDocumentView.ApplyViewState
title: IOleDocumentView::ApplyViewState (docobj.h)
description: Initializes a view with view state previously saved in call to IOleDocumentView::SaveViewState.
helpviewer_keywords: ["ApplyViewState","ApplyViewState method [COM]","ApplyViewState method [COM]","IOleDocumentView interface","IOleDocumentView interface [COM]","ApplyViewState method","IOleDocumentView.ApplyViewState","IOleDocumentView::ApplyViewState","_ole_ioledocumentview_applyviewstate","com.ioledocumentview_applyviewstate","docobj/IOleDocumentView::ApplyViewState"]
old-location: com\ioledocumentview_applyviewstate.htm
tech.root: com
ms.assetid: f78526b4-977a-4dde-8a2f-7ae0a1c5c7f9
ms.date: 12/05/2018
ms.keywords: ApplyViewState, ApplyViewState method [COM], ApplyViewState method [COM],IOleDocumentView interface, IOleDocumentView interface [COM],ApplyViewState method, IOleDocumentView.ApplyViewState, IOleDocumentView::ApplyViewState, _ole_ioledocumentview_applyviewstate, com.ioledocumentview_applyviewstate, docobj/IOleDocumentView::ApplyViewState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleDocumentView::ApplyViewState
 - docobj/IOleDocumentView::ApplyViewState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocumentView.ApplyViewState
---

# IOleDocumentView::ApplyViewState


## -description

Initializes a view with view state previously saved in call to <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-saveviewstate">IOleDocumentView::SaveViewState</a>.

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

<a href="/windows/desktop/api/docobj/nf-docobj-ioledocument-createview">IOleDocument::CreateView</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-saveviewstate">IOleDocumentView::SaveViewState</a>