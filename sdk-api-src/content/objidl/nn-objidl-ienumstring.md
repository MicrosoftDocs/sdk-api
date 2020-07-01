---
UID: NN:objidl.IEnumString
title: IEnumString (objidl.h)
description: Enumerate strings. LPWSTR is the type that indicates a pointer to a zero-terminated string of wide, or Unicode, characters.
helpviewer_keywords: ["IEnumString","IEnumString interface [COM]","IEnumString interface [COM]","described","_com_ienumstring","com.ienumstring","objidlbase/IEnumString"]
old-location: com\ienumstring.htm
tech.root: com
ms.assetid: 7f3e642a-17c7-4646-8c70-da6b0946a415
ms.date: 12/05/2018
ms.keywords: IEnumString, IEnumString interface [COM], IEnumString interface [COM],described, _com_ienumstring, com.ienumstring, objidlbase/IEnumString
f1_keywords:
- objidl/IEnumString
dev_langs:
- c++
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
- objidlbase.h
api_name:
- IEnumString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumString interface


## -description


Enumerate strings. <b>LPWSTR</b> is the type that indicates a pointer to a zero-terminated string of wide, or Unicode, characters.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumString</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumString</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumString</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstring-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstring-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstring-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstring-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

