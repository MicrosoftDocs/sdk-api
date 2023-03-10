---
UID: NE:ocidl.tagUASFLAGS
title: UASFLAGS (ocidl.h)
description: Provides information about the parent undo unit.
helpviewer_keywords: ["UASFLAGS","UASFLAGS enumeration [COM]","UAS_BLOCKED","UAS_MASK","UAS_NOPARENTENABLE","UAS_NORMAL","_ole_UASFLAGS","com.uasflags","ocidl/UASFLAGS","ocidl/UAS_BLOCKED","ocidl/UAS_MASK","ocidl/UAS_NOPARENTENABLE","ocidl/UAS_NORMAL"]
old-location: com\uasflags.htm
tech.root: com
ms.assetid: cf711180-e38a-4cff-bd2d-2cfca41b376d
ms.date: 12/05/2018
ms.keywords: UASFLAGS, UASFLAGS enumeration [COM], UAS_BLOCKED, UAS_MASK, UAS_NOPARENTENABLE, UAS_NORMAL, _ole_UASFLAGS, com.uasflags, ocidl/UASFLAGS, ocidl/UAS_BLOCKED, ocidl/UAS_MASK, ocidl/UAS_NOPARENTENABLE, ocidl/UAS_NORMAL
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
targetos: Windows
req.typenames: UASFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUASFLAGS
 - ocidl/tagUASFLAGS
 - UASFLAGS
 - ocidl/UASFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - UASFLAGS
---

# UASFLAGS enumeration


## -description

Provides information about the parent undo unit.

## -enum-fields

### -field UAS_NORMAL:0

The currently open parent undo unit is in a normal, unblocked state and can accept any new units added through calls to its <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-open">Open</a> or <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-add">Add</a> methods.

### -field UAS_BLOCKED:0x1

The currently open undo unit is blocked and will reject any undo units added through calls to its <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-open">IOleParentUndoUnit::Open</a> or <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-add">IOleParentUndoUnit::Add</a> methods. The caller need not create any new units since they will just be rejected.

### -field UAS_NOPARENTENABLE:0x2

The currently open undo unit will accept new units, but the caller should act like there is no currently open unit. This means that if the new unit being created requires a parent, then this parent does not satisfy that requirement and the undo stack should be cleared.

### -field UAS_MASK:0x3

When checking for a normal state, use this value to mask unused bits in the <i>pdwState</i> parameter to the <a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-getparentstate">IOleParentUndoUnit::GetParentState</a> method for future compatibility. For example:


``` syntax
fNormal = ((pdwState &amp; UAS_MASK) == UAS_NORMAL)
```


## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ioleparentundounit-getparentstate">IOleParentUndoUnit::GetParentState</a>
