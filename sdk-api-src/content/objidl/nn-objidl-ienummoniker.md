---
UID: NN:objidl.IEnumMoniker
title: IEnumMoniker (objidl.h)
description: Enumerates the components of a moniker or the monikers in a table of monikers.
helpviewer_keywords: ["IEnumMoniker","IEnumMoniker interface [COM]","IEnumMoniker interface [COM]","described","_ole_ienummoniker","com.ienummoniker","objidl/IEnumMoniker"]
old-location: com\ienummoniker.htm
tech.root: com
ms.assetid: c8dec22b-946d-48ae-9315-54d353f3b853
ms.date: 12/05/2018
ms.keywords: IEnumMoniker, IEnumMoniker interface [COM], IEnumMoniker interface [COM],described, _ole_ienummoniker, com.ienummoniker, objidl/IEnumMoniker
req.header: objidl.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumMoniker
 - objidl/IEnumMoniker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IEnumMoniker
---

# IEnumMoniker interface


## -description

Enumerates the components of a moniker or the monikers in a table of monikers.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumMoniker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumMoniker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumMoniker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienummoniker-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienummoniker-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienummoniker-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienummoniker-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-enum">IMoniker::Enum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-enumrunning">IRunningObjectTable::EnumRunning</a>

