---
UID: NN:ocidl.IEnumOleUndoUnits
title: IEnumOleUndoUnits
author: windows-sdk-content
description: Enumerates the undo units on the undo or redo stack.
old-location: com\ienumoleundounits.htm
tech.root: com
ms.assetid: f43cbd9d-d91b-4230-816f-693dec7056a4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumOleUndoUnits, IEnumOleUndoUnits interface [COM], IEnumOleUndoUnits interface [COM],described, _ole_ienumoleundounits, com.ienumoleundounits, ocidl/IEnumOleUndoUnits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumOleUndoUnits interface


## -description


Enumerates the undo units on the undo or redo stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOleUndoUnits</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IEnumOleUndoUnits</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/637c3299-816f-4f3c-9758-b3200b5cf153">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/041c3f20-bd8c-482d-9716-99f49a6bc902">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f079c166-c4a8-4827-a8c5-3c5e0cb13b77">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fdf81ee-df31-4702-8b5e-f540ca3e6602">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>



<a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a>
 

 

