---
UID: NN:ocidl.IEnumOleUndoUnits
title: IEnumOleUndoUnits
author: windows-driver-content
description: Enumerates the undo units on the undo or redo stack.
old-location: com\ienumoleundounits.htm
old-project: com
ms.assetid: f43cbd9d-d91b-4230-816f-693dec7056a4
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IEnumOleUndoUnits, IEnumOleUndoUnits interface [COM], IEnumOleUndoUnits interface [COM], described, _ole_ienumoleundounits, com.ienumoleundounits, ocidl/IEnumOleUndoUnits
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IEnumOleUndoUnits
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumOleUndoUnits interface


## -description


Enumerates the undo units on the undo or redo stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOleUndoUnits</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IEnumOleUndoUnits</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0f507506-3589-4d5b-b1b3-010bce9ae42f">IOleUndoManager</a>



<a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a>
 

 

