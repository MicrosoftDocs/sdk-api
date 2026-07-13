---
UID: NE:directmanipulation.DIRECTMANIPULATION_MOTION_TYPES
title: DIRECTMANIPULATION_MOTION_TYPES (directmanipulation.h)
description: Defines the Direct Manipulation motion type.
helpviewer_keywords: ["DIRECTMANIPULATION_MOTION_ALL","DIRECTMANIPULATION_MOTION_CENTERX","DIRECTMANIPULATION_MOTION_CENTERY","DIRECTMANIPULATION_MOTION_NONE","DIRECTMANIPULATION_MOTION_TRANSLATEX","DIRECTMANIPULATION_MOTION_TRANSLATEY","DIRECTMANIPULATION_MOTION_TYPES","DIRECTMANIPULATION_MOTION_TYPES enumeration [Direct Manipulation]","DIRECTMANIPULATION_MOTION_ZOOM","directmanipulation.directmanipulation_motion_types","directmanipulation/DIRECTMANIPULATION_MOTION_ALL","directmanipulation/DIRECTMANIPULATION_MOTION_CENTERX","directmanipulation/DIRECTMANIPULATION_MOTION_CENTERY","directmanipulation/DIRECTMANIPULATION_MOTION_NONE","directmanipulation/DIRECTMANIPULATION_MOTION_TRANSLATEX","directmanipulation/DIRECTMANIPULATION_MOTION_TRANSLATEY","directmanipulation/DIRECTMANIPULATION_MOTION_TYPES","directmanipulation/DIRECTMANIPULATION_MOTION_ZOOM"]
old-location: directmanipulation\directmanipulation_motion_types.htm
tech.root: directmanipulation
ms.assetid: a0b4da55-3ebb-4281-a372-4bc6b91e6789
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_MOTION_ALL, DIRECTMANIPULATION_MOTION_CENTERX, DIRECTMANIPULATION_MOTION_CENTERY, DIRECTMANIPULATION_MOTION_NONE, DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_MOTION_TRANSLATEY, DIRECTMANIPULATION_MOTION_TYPES, DIRECTMANIPULATION_MOTION_TYPES enumeration [Direct Manipulation], DIRECTMANIPULATION_MOTION_ZOOM, directmanipulation.directmanipulation_motion_types, directmanipulation/DIRECTMANIPULATION_MOTION_ALL, directmanipulation/DIRECTMANIPULATION_MOTION_CENTERX, directmanipulation/DIRECTMANIPULATION_MOTION_CENTERY, directmanipulation/DIRECTMANIPULATION_MOTION_NONE, directmanipulation/DIRECTMANIPULATION_MOTION_TRANSLATEX, directmanipulation/DIRECTMANIPULATION_MOTION_TRANSLATEY, directmanipulation/DIRECTMANIPULATION_MOTION_TYPES, directmanipulation/DIRECTMANIPULATION_MOTION_ZOOM
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIRECTMANIPULATION_MOTION_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_MOTION_TYPES
 - directmanipulation/DIRECTMANIPULATION_MOTION_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_MOTION_TYPES
---

# DIRECTMANIPULATION_MOTION_TYPES enumeration


## -description

Defines the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> motion type.

## -enum-fields

### -field DIRECTMANIPULATION_MOTION_NONE:0

None.

### -field DIRECTMANIPULATION_MOTION_TRANSLATEX:0x1

Translation in the horizontal axis.

### -field DIRECTMANIPULATION_MOTION_TRANSLATEY:0x2

Translation in the vertical axis.

### -field DIRECTMANIPULATION_MOTION_ZOOM:0x4

Zoom.

### -field DIRECTMANIPULATION_MOTION_CENTERX:0x10

The horizontal center of the manipulation.

### -field DIRECTMANIPULATION_MOTION_CENTERY:0x20

The vertical center of the manipulation.

### -field DIRECTMANIPULATION_MOTION_ALL

All manipulation motion.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining">SetChaining</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval">SetSnapInterval</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints">SetSnapPoints</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnaptype">SetSnapType</a>
