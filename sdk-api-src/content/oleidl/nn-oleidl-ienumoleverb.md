---
UID: NN:oleidl.IEnumOLEVERB
title: IEnumOLEVERB (oleidl.h)
description: Enumerates the different verbs available for an object in order of ascending verb number. An enumerator that implements the IEnumOLEVERB interface is returned by IOleObject::EnumVerbs.helpviewer_keywords: ["IEnumOLEVERB","IEnumOLEVERB interface [COM]","IEnumOLEVERB interface [COM]","described","_ole_ienumoleverb","com.ienumoleverb","oleidl/IEnumOLEVERB"]
old-location: com\ienumoleverb.htm
tech.root: com
ms.assetid: fc9b3474-6f56-4274-af7d-72e0920c0457
ms.date: 12/05/2018
ms.keywords: IEnumOLEVERB, IEnumOLEVERB interface [COM], IEnumOLEVERB interface [COM],described, _ole_ienumoleverb, com.ienumoleverb, oleidl/IEnumOLEVERB
f1_keywords:
- oleidl/IEnumOLEVERB
dev_langs:
- c++
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
- OleIdl.h
api_name:
- IEnumOLEVERB
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumOLEVERB interface


## -description


Enumerates the different verbs available for an object in order of ascending verb number. An enumerator that implements the <b>IEnumOLEVERB</b> interface is returned by <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOLEVERB</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumOLEVERB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumOLEVERB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ienumoleverb-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ienumoleverb-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ienumoleverb-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ienumoleverb-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

