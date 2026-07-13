---
UID: NE:objidl.tagMKSYS
title: MKSYS (objidl.h)
description: Indicates the moniker's class.
helpviewer_keywords: ["MKSYS","MKSYS enumeration [COM]","MKSYS_ANTIMONIKER","MKSYS_CLASSMONIKER","MKSYS_FILEMONIKER","MKSYS_GENERICCOMPOSITE","MKSYS_ITEMMONIKER","MKSYS_LUAMONIKER","MKSYS_NONE","MKSYS_OBJREFMONIKER","MKSYS_POINTERMONIKER","MKSYS_SESSIONMONIKER","_com_MKSYS","com.mksys","objidl/MKSYS","objidl/MKSYS_ANTIMONIKER","objidl/MKSYS_CLASSMONIKER","objidl/MKSYS_FILEMONIKER","objidl/MKSYS_GENERICCOMPOSITE","objidl/MKSYS_ITEMMONIKER","objidl/MKSYS_LUAMONIKER","objidl/MKSYS_NONE","objidl/MKSYS_OBJREFMONIKER","objidl/MKSYS_POINTERMONIKER","objidl/MKSYS_SESSIONMONIKER"]
old-location: com\mksys.htm
tech.root: com
ms.assetid: f0d8ab71-5be9-4a5c-a036-d3a0a90a053f
ms.date: 12/05/2018
ms.keywords: MKSYS, MKSYS enumeration [COM], MKSYS_ANTIMONIKER, MKSYS_CLASSMONIKER, MKSYS_FILEMONIKER, MKSYS_GENERICCOMPOSITE, MKSYS_ITEMMONIKER, MKSYS_LUAMONIKER, MKSYS_NONE, MKSYS_OBJREFMONIKER, MKSYS_POINTERMONIKER, MKSYS_SESSIONMONIKER, _com_MKSYS, com.mksys, objidl/MKSYS, objidl/MKSYS_ANTIMONIKER, objidl/MKSYS_CLASSMONIKER, objidl/MKSYS_FILEMONIKER, objidl/MKSYS_GENERICCOMPOSITE, objidl/MKSYS_ITEMMONIKER, objidl/MKSYS_LUAMONIKER, objidl/MKSYS_NONE, objidl/MKSYS_OBJREFMONIKER, objidl/MKSYS_POINTERMONIKER, objidl/MKSYS_SESSIONMONIKER
req.header: objidl.h
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
req.typenames: MKSYS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMKSYS
 - objidl/tagMKSYS
 - MKSYS
 - objidl/MKSYS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - MKSYS
---

# MKSYS enumeration


## -description

Indicates the moniker's class.

## -enum-fields

### -field MKSYS_NONE:0

Indicates a custom moniker implementation.

### -field MKSYS_GENERICCOMPOSITE:1

Indicates the system's generic composite moniker class.

### -field MKSYS_FILEMONIKER:2

Indicates the system's file moniker class.

### -field MKSYS_ANTIMONIKER:3

Indicates the system's anti-moniker class.

### -field MKSYS_ITEMMONIKER:4

Indicates the system's item moniker class.

### -field MKSYS_POINTERMONIKER:5

Indicates the system's pointer moniker class.

### -field MKSYS_CLASSMONIKER:7

Indicates the system's class moniker class.

### -field MKSYS_OBJREFMONIKER:8

Indicates the system's OBJREF moniker class.

### -field MKSYS_SESSIONMONIKER:9

Indicates the system's terminal server session moniker class.

### -field MKSYS_LUAMONIKER:10

Indicates the system's elevation moniker class.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-issystemmoniker">IMoniker::IsSystemMoniker</a>
