---
UID: NF:docobj.IEnumOleDocumentViews.Clone
title: IEnumOleDocumentViews::Clone (docobj.h)
description: Creates a new enumerator that contains the same enumeration state as the current one. (IEnumOleDocumentViews.Clone)
helpviewer_keywords: ["Clone","Clone method [COM]","Clone method [COM]","IEnumOleDocumentViews interface","IEnumOleDocumentViews interface [COM]","Clone method","IEnumOleDocumentViews.Clone","IEnumOleDocumentViews::Clone","_ole_ienumoledocumentviews_clone","com.ienumoledocumentviews_clone","docobj/IEnumOleDocumentViews::Clone"]
old-location: com\ienumoledocumentviews_clone.htm
tech.root: com
ms.assetid: f3d6eaaf-455a-4d66-87d2-ba19a1db1faf
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumOleDocumentViews interface, IEnumOleDocumentViews interface [COM],Clone method, IEnumOleDocumentViews.Clone, IEnumOleDocumentViews::Clone, _ole_ienumoledocumentviews_clone, com.ienumoledocumentviews_clone, docobj/IEnumOleDocumentViews::Clone
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
 - IEnumOleDocumentViews::Clone
 - docobj/IEnumOleDocumentViews::Clone
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
 - IEnumOleDocumentViews.Clone
---

# IEnumOleDocumentViews::Clone


## -description

Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.

## -parameters

### -param ppEnum [out]

A pointer to the <a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a> interface pointer on the newly created enumerator. The caller must release this enumerator separately from the one from which it was cloned.

## -returns

This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified enumerator is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-ienumoledocumentviews">IEnumOleDocumentViews</a>
