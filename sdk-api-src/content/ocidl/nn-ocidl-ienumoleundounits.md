---
UID: NN:ocidl.IEnumOleUndoUnits
title: IEnumOleUndoUnits (ocidl.h)
description: Enumerates the undo units on the undo or redo stack.
helpviewer_keywords: ["IEnumOleUndoUnits","IEnumOleUndoUnits interface [COM]","IEnumOleUndoUnits interface [COM]","described","_ole_ienumoleundounits","com.ienumoleundounits","ocidl/IEnumOleUndoUnits"]
old-location: com\ienumoleundounits.htm
tech.root: com
ms.assetid: f43cbd9d-d91b-4230-816f-693dec7056a4
ms.date: 12/05/2018
ms.keywords: IEnumOleUndoUnits, IEnumOleUndoUnits interface [COM], IEnumOleUndoUnits interface [COM],described, _ole_ienumoleundounits, com.ienumoleundounits, ocidl/IEnumOleUndoUnits
f1_keywords:
- ocidl/IEnumOleUndoUnits
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
- OCIdl.h
api_name:
- IEnumOleUndoUnits
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumOleUndoUnits interface


## -description


Enumerates the undo units on the undo or redo stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOleUndoUnits</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumOleUndoUnits</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumOleUndoUnits</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumformatetc-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumformatetc-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumformatetc-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumformatetc-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a>
 

 

