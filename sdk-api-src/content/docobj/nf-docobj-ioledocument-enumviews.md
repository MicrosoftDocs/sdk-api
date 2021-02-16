---
UID: NF:docobj.IOleDocument.EnumViews
title: IOleDocument::EnumViews (docobj.h)
description: Creates an object that enumerates the views supported by a document object, or if only one view is supported, returns a pointer to that view.
helpviewer_keywords: ["EnumViews","EnumViews method [COM]","EnumViews method [COM]","IOleDocument interface","IOleDocument interface [COM]","EnumViews method","IOleDocument.EnumViews","IOleDocument::EnumViews","_ole_ioledocument_enumviews","com.ioledocument_enumviews","docobj/IOleDocument::EnumViews"]
old-location: com\ioledocument_enumviews.htm
tech.root: com
ms.assetid: ca186853-0792-4a34-b718-46927a73e670
ms.date: 12/05/2018
ms.keywords: EnumViews, EnumViews method [COM], EnumViews method [COM],IOleDocument interface, IOleDocument interface [COM],EnumViews method, IOleDocument.EnumViews, IOleDocument::EnumViews, _ole_ioledocument_enumviews, com.ioledocument_enumviews, docobj/IOleDocument::EnumViews
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
 - IOleDocument::EnumViews
 - docobj/IOleDocument::EnumViews
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
 - IOleDocument.EnumViews
---

# IOleDocument::EnumViews


## -description

Creates an object that enumerates the views supported by a document object, or if only one view is supported, returns a pointer to that view.

## -parameters

### -param ppEnum [out]

A pointer to an <a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a> pointer variable that receives the interface pointer to the enumerator object.

### -param ppView [out]

A pointer to an <a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a> pointer variable that receives the interface pointer to a single view object.

## -returns

This method returns S_OK if the object supports multiple views, then <i>ppEnum</i> contains a pointer to the enumerator object, and <i>ppView</i> is <b>NULL</b>. Otherwise, <i>ppEnum</i> is <b>NULL</b>, and <i>ppView</i> contains an interface pointer on the single view.

Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppEnum</i> or <i>ppView</i> is invalid. The caller must pass valid pointers for both arguments.

</td>
</tr>
</table>

## -remarks

If a document object supports multiple views of its data, it must also implement <a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a> and pass that interface's pointer in the out parameter <i>ppEnum</i>. Using this pointer, the container can enumerate the views supported by the document object.

If the document object supports only a single view, <b>IOleDocument::EnumViews</b> passes that view's <a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a> pointer in the out parameter <i>ppView</i>.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocument">IOleDocument</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>