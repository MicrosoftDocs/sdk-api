---
UID: NE:objidl.tagMKSYS
title: MKSYS (objidl.h)
description: Indicates the moniker's class.
old-location: com\mksys.htm
tech.root: com
ms.assetid: f0d8ab71-5be9-4a5c-a036-d3a0a90a053f
ms.date: 12/05/2018
ms.keywords: MKSYS, MKSYS enumeration [COM], MKSYS_ANTIMONIKER, MKSYS_CLASSMONIKER, MKSYS_FILEMONIKER, MKSYS_GENERICCOMPOSITE, MKSYS_ITEMMONIKER, MKSYS_LUAMONIKER, MKSYS_NONE, MKSYS_OBJREFMONIKER, MKSYS_POINTERMONIKER, MKSYS_SESSIONMONIKER, _com_MKSYS, com.mksys, objidl/MKSYS, objidl/MKSYS_ANTIMONIKER, objidl/MKSYS_CLASSMONIKER, objidl/MKSYS_FILEMONIKER, objidl/MKSYS_GENERICCOMPOSITE, objidl/MKSYS_ITEMMONIKER, objidl/MKSYS_LUAMONIKER, objidl/MKSYS_NONE, objidl/MKSYS_OBJREFMONIKER, objidl/MKSYS_POINTERMONIKER, objidl/MKSYS_SESSIONMONIKER
f1_keywords:
- objidl/MKSYS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Objidl.h
api_name:
- MKSYS
targetos: Windows
req.typenames: MKSYS
req.redist: 
ms.custom: 19H1
---

# MKSYS enumeration


## -description


Indicates the moniker's class.


## -enum-fields




### -field MKSYS_NONE

Indicates a custom moniker implementation.


### -field MKSYS_GENERICCOMPOSITE

Indicates the system's generic composite moniker class.


### -field MKSYS_FILEMONIKER

Indicates the system's file moniker class.


### -field MKSYS_ANTIMONIKER

Indicates the system's anti-moniker class.


### -field MKSYS_ITEMMONIKER

Indicates the system's item moniker class.


### -field MKSYS_POINTERMONIKER

Indicates the system's pointer moniker class.


### -field MKSYS_CLASSMONIKER

Indicates the system's class moniker class.


### -field MKSYS_OBJREFMONIKER

Indicates the system's OBJREF moniker class.


### -field MKSYS_SESSIONMONIKER

Indicates the system's terminal server session moniker class.


### -field MKSYS_LUAMONIKER

Indicates the system's elevation moniker class.

## Remark

MKSYS_URLMONIKER is an additional value.

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-issystemmoniker">IMoniker::IsSystemMoniker</a>
 

 

