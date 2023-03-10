---
UID: NF:docobj.IOleDocumentView.SaveViewState
title: IOleDocumentView::SaveViewState (docobj.h)
description: Saves the view state into the specified stream.
helpviewer_keywords: ["IOleDocumentView interface [COM]","SaveViewState method","IOleDocumentView.SaveViewState","IOleDocumentView::SaveViewState","SaveViewState","SaveViewState method [COM]","SaveViewState method [COM]","IOleDocumentView interface","_ole_ioledocumentview_saveviewstate","com.ioledocumentview_saveviewstate","docobj/IOleDocumentView::SaveViewState"]
old-location: com\ioledocumentview_saveviewstate.htm
tech.root: com
ms.assetid: d270b441-d0d5-4dd5-995b-6ca5738747c5
ms.date: 12/05/2018
ms.keywords: IOleDocumentView interface [COM],SaveViewState method, IOleDocumentView.SaveViewState, IOleDocumentView::SaveViewState, SaveViewState, SaveViewState method [COM], SaveViewState method [COM],IOleDocumentView interface, _ole_ioledocumentview_saveviewstate, com.ioledocumentview_saveviewstate, docobj/IOleDocumentView::SaveViewState
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
 - IOleDocumentView::SaveViewState
 - docobj/IOleDocumentView::SaveViewState
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
 - IOleDocumentView.SaveViewState
---

# IOleDocumentView::SaveViewState


## -description

Saves the view state into the specified stream.

## -parameters

### -param pstm [in]

 A pointer to the stream in which the view is to save its state data.

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
The value in pstm is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This view has no meaningful state to save. This error should be rare because most views have at least some state information worth saving.

</td>
</tr>
</table>

## -remarks

The view's state includes properties such as the view type, zoom factor, and location of insertion point. The container typically calls this function before deactivating the view. The stream can then later be used to reinitialize a view of the same document to this saved state through <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-applyviewstate">IOleDocumentView::ApplyViewState</a>.

According to the rules governing <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>, a view must write its CLSID as the first element in the stream. Any cross-platform file format compatibility issues that apply to the document's storage representation also apply to this context.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-applyviewstate">IOleDocumentView::ApplyViewState</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>