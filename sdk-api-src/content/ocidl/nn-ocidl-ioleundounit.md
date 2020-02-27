---
UID: NN:ocidl.IOleUndoUnit
title: IOleUndoUnit (ocidl.h)
description: Serves as the main interface on an undo unit. An undo unit encapsulates the information necessary to undo or redo a single action.
old-location: com\ioleundounit.htm
tech.root: com
ms.assetid: 0822c894-b96c-4b69-94d2-b052dff81f6e
ms.date: 12/05/2018
ms.keywords: IOleUndoUnit, IOleUndoUnit interface [COM], IOleUndoUnit interface [COM],described, _ole_ioleundounit, com.ioleundounit, ocidl/IOleUndoUnit
f1_keywords:
- ocidl/IOleUndoUnit
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
- IOleUndoUnit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleUndoUnit interface


## -description


Serves as the main interface on an undo unit. An undo unit encapsulates the information necessary to undo or redo a single action.

When an object's state changes and it needs to create an undo unit, it first needs to know what parent units are open. It calls the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-getopenparentstate">IOleUndoManager::GetOpenParentState</a> method to determine this. If the call returns S_FALSE, then there is no enabling parent. If the call returns S_OK but the UAS_NOPARENTENABLE flag is set, then the open parent is a disabling parent. In either of these cases, the object calls <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-discardfrom">IOleUndoManager::DiscardFrom</a>(NULL) on the undo manager and skips creating the undo unit.

If the method returns S_OK, but the UAS_BLOCKED flag is set, then the open parent is a blocking parent. The object does not need to create an undo unit, since it would be immediately discarded. If the return value is S_OK and neither of the bit flags are set, then the object creates the undo unit and calls <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add">IOleUndoManager::Add</a> on the undo manager.

The object should retain a pointer to the undo manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUndoUnit</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleUndoUnit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUndoUnit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundounit-do">Do</a>
</td>
<td align="left" width="63%">
Instructs the undo unit to carry out its action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundounit-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the undo unit that can be used in the undo or redo user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundounit-getunittype">GetUnitType</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID and a type identifier for the undo unit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ioleundounit-onnextadd">OnNextAdd</a>
</td>
<td align="left" width="63%">
Notifies the last undo unit in the collection that a new unit has been added.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit">IOleParentUndoUnit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>
 

 

