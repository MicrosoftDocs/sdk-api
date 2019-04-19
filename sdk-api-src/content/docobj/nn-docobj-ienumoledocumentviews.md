---
UID: NN:docobj.IEnumOleDocumentViews
title: IEnumOleDocumentViews (docobj.h)
author: windows-sdk-content
description: Enumerates the views supported by a document object.
old-location: com\ienumoledocumentviews.htm
tech.root: com
ms.assetid: cd8fa8b8-17b1-4d77-9611-473725899351
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumOleDocumentViews, IEnumOleDocumentViews interface [COM], IEnumOleDocumentViews interface [COM],described, _ole_ienumoledocumentviews, com.ienumoledocumentviews, docobj/IEnumOleDocumentViews
ms.topic: interface
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
 - IEnumOleDocumentViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumOleDocumentViews interface


## -description


Enumerates the views supported by a document object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOleDocumentViews</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IEnumOleDocumentViews</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f3d6eaaf-455a-4d66-87d2-ba19a1db1faf">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a58131bf-88ff-4661-9047-2d70b5e7931b">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9dbdf36-fff1-4cd5-a890-219c8311dadf">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea853e5a-ea73-441f-9b13-0425a4d734ad">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

