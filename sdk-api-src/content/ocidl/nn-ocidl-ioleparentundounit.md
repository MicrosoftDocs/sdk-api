---
UID: NN:ocidl.IOleParentUndoUnit
title: IOleParentUndoUnit (ocidl.h)
description: Enables undo units to contain child undo units.
helpviewer_keywords: ["IOleParentUndoUnit","IOleParentUndoUnit interface [COM]","IOleParentUndoUnit interface [COM]","described","_ole_ioleparentundounit","com.ioleparentundounit","ocidl/IOleParentUndoUnit"]
old-location: com\ioleparentundounit.htm
tech.root: com
ms.assetid: 4407d673-286a-4221-ae35-09b9865161f8
ms.date: 12/05/2018
ms.keywords: IOleParentUndoUnit, IOleParentUndoUnit interface [COM], IOleParentUndoUnit interface [COM],described, _ole_ioleparentundounit, com.ioleparentundounit, ocidl/IOleParentUndoUnit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleParentUndoUnit
 - ocidl/IOleParentUndoUnit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleParentUndoUnit
---

# IOleParentUndoUnit interface


## -description

Enables undo units to contain child undo units. For example, a complex action can be presented to the end user as a single undo action even though a number of separate actions are involved. All the subordinate undo actions are contained within the top-level, parent undo unit.

A parent undo unit is initially created using the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-open">IOleUndoManager::Open method</a>. The addition of undo units should always be done through the undo manager. The <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-open">IOleParentUndoUnit::Open</a> and <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-close">IOleParentUndoUnit::Close</a> methods on parent units will end up being called by the undo manager. Having parent units call back into the undo manager will cause infinite recursion.

While a parent unit is open, the undo manager adds undo units to it by calling <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-add">IOleParentUndoUnit::Add</a>. When the undo manager closes a top-level parent, the entire undo unit with its nested subordinates is placed on top of the undo stack.

An enabling parent is required to be open on the stack before any other undo units can be added. If one isn't open, the stack should be cleared instead. This is to ensure that undo units only get added as a result of user actions and not programmatic actions. For example, if your application wants to make clicking a certain button undoable, but that same action is also exposed through the object model. That action should be undoable through the user interface but not the object model because you cannot restore the state of the user's script code. Because the same code implements the change in both cases, the UI code that handles the button click should open an enabling parent on the stack, call the appropriate code, and then close the parent unit. The object model code would not open a parent unit, causing the undo stack to be cleared.

A blocking parent is used when you do not want your code to call other code that you know may try to add undo units to the stack. For example, you should use a blocking parent if you call code that creates undo units, that your outer code has already created that will fully undo all the desired behavior.

A non-enabling parent is used when you fire an event in response to a user action. The stack would be cleared only if the event handler did something that tried to create an undo unit, but if no handler exists then the undo stack would be preserved.

If an object needs to create a parent unit, there are several cases to consider:
<ul>
<li>To create an enabling parent unit, the object calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-getopenparentstate">IOleUndoManager::GetOpenParentState</a> on the undo manager and checks the return value. If the value is S_FALSE, then the object creates the enabling parent and opens it. If the return value is S_OK, then there is a parent already open. If the open parent is blocked (UAS_BLOCKED bit set), or an enabling parent (UAS_BLOCKED and UAS_NOPARENTENABLE bits not set), then there is no need to create the enabling parent. If the currently open parent is a disabling parent (UAS_NOPARENTENABLE bit set), then the enabling parent should be created and opened to re-enable adding undo units. Note that UAS_NORMAL has a value of zero, which means it is the absence of all other bits and is not a bit flag that can be set. If comparing *<i>pdwState</i> against UAS_NORMAL, mask out unused bits from <i>pdwState</i> with UAS_MASK to allow for future expansion.</li>
<li>To create a blocked parent, the object calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-getopenparentstate">IOleUndoManager::GetOpenParentState</a> and checks for an open parent that is already blocked. If one exists, then there is no need to create the new blocking parent. Otherwise, the object creates it and opens it on the stack.</li>
<li>To create a disabling parent, the object calls <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-getopenparentstate">IOleUndoManager::GetOpenParentState</a> and checks for an open parent that is blocked or disabling. If either one exists it is unnecessary to create the new parent. Otherwise, the object creates the parent and opens it on the stack.</li>
</ul>In the event that both the UAS_NOPARENTENABLE and UAS_BLOCKED flags are set, the flag that is most relevant to the caller should be used with UAS_NOPARENTENABLE taking precedence. For example, if an object is creating a simple undo unit, it should pay attention to the UAS_NOPARENTENABLE flag and clear the undo stack. If it is creating an enabling parent unit, then it should pay attention to the UAS_BLOCKED flag and skip the creation.

When the parent undo unit is marked blocked, it discards any undo units it receives.

## -inheritance

The <b>IOleParentUndoUnit</b> interface inherits from <b>IOleUndoUnit</b>. <b>IOleParentUndoUnit</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundounit">IOleUndoUnit</a>
