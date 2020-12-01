---
UID: NN:docobj.IEnumOleDocumentViews
title: IEnumOleDocumentViews (docobj.h)
description: Enumerates the views supported by a document object.
helpviewer_keywords: ["IEnumOleDocumentViews","IEnumOleDocumentViews interface [COM]","IEnumOleDocumentViews interface [COM]","described","_ole_ienumoledocumentviews","com.ienumoledocumentviews","docobj/IEnumOleDocumentViews"]
old-location: com\ienumoledocumentviews.htm
tech.root: com
ms.assetid: cd8fa8b8-17b1-4d77-9611-473725899351
ms.date: 12/05/2018
ms.keywords: IEnumOleDocumentViews, IEnumOleDocumentViews interface [COM], IEnumOleDocumentViews interface [COM],described, _ole_ienumoledocumentviews, com.ienumoledocumentviews, docobj/IEnumOleDocumentViews
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
 - IEnumOleDocumentViews
 - docobj/IEnumOleDocumentViews
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
 - IEnumOleDocumentViews
---

# IEnumOleDocumentViews interface


## -description

Enumerates the views supported by a document object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOleDocumentViews</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumOleDocumentViews</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumOleDocumentViews</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/docobj/nf-docobj-ienumoledocumentviews-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/docobj/nf-docobj-ienumoledocumentviews-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/docobj/nf-docobj-ienumoledocumentviews-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/docobj/nf-docobj-ienumoledocumentviews-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table>