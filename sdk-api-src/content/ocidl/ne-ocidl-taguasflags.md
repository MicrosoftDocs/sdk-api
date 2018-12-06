---
UID: NE:ocidl.tagUASFLAGS
title: tagUASFLAGS
author: windows-sdk-content
description: Provides information about the parent undo unit.
old-location: com\uasflags.htm
tech.root: com
ms.assetid: cf711180-e38a-4cff-bd2d-2cfca41b376d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UASFLAGS, UASFLAGS enumeration [COM], UAS_BLOCKED, UAS_MASK, UAS_NOPARENTENABLE, UAS_NORMAL, _ole_UASFLAGS, com.uasflags, ocidl/UASFLAGS, ocidl/UAS_BLOCKED, ocidl/UAS_MASK, ocidl/UAS_NOPARENTENABLE, ocidl/UAS_NORMAL, tagUASFLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - UASFLAGS
product: Windows
targetos: Windows
req.typenames: UASFLAGS
req.redist: 
---

# tagUASFLAGS enumeration


## -description


Provides information about the parent undo unit.


## -enum-fields




### -field UAS_NORMAL

The currently open parent undo unit is in a normal, unblocked state and can accept any new units added through calls to its <a href="https://msdn.microsoft.com/185eae3b-5323-45f1-9810-47bd21ce0d22">Open</a> or <a href="https://msdn.microsoft.com/86db3308-6f01-47f1-ba28-3ed5e70b7cb9">Add</a> methods.


### -field UAS_BLOCKED

The currently open undo unit is blocked and will reject any undo units added through calls to its <a href="https://msdn.microsoft.com/185eae3b-5323-45f1-9810-47bd21ce0d22">IOleParentUndoUnit::Open</a> or <a href="https://msdn.microsoft.com/86db3308-6f01-47f1-ba28-3ed5e70b7cb9">IOleParentUndoUnit::Add</a> methods. The caller need not create any new units since they will just be rejected.


### -field UAS_NOPARENTENABLE

The currently open undo unit will accept new units, but the caller should act like there is no currently open unit. This means that if the new unit being created requires a parent, then this parent does not satisfy that requirement and the undo stack should be cleared.


### -field UAS_MASK

When checking for a normal state, use this value to mask unused bits in the <i>pdwState</i> parameter to the <a href="https://msdn.microsoft.com/23eb1768-b68a-4b97-94a4-eeb7b840dda8">IOleParentUndoUnit::GetParentState</a> method for future compatibility. For example:

<pre class="syntax" xml:space="preserve"><code>fNormal = ((pdwState &amp; UAS_MASK) == UAS_NORMAL)</code></pre>

## -see-also




<a href="https://msdn.microsoft.com/23eb1768-b68a-4b97-94a4-eeb7b840dda8">IOleParentUndoUnit::GetParentState</a>
 

 

