---
UID: NE:directmanipulation.DIRECTMANIPULATION_SNAPPOINT_TYPE
title: DIRECTMANIPULATION_SNAPPOINT_TYPE (directmanipulation.h)
description: Modifies how the final inertia end position is calculated.
helpviewer_keywords: ["DIRECTMANIPULATION_SNAPPOINT_MANDATORY","DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE","DIRECTMANIPULATION_SNAPPOINT_OPTIONAL","DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE","DIRECTMANIPULATION_SNAPPOINT_TYPE","DIRECTMANIPULATION_SNAPPOINT_TYPE enumeration [Direct Manipulation]","directmanipulation.directmanipulation_snappoint_type","directmanipulation/DIRECTMANIPULATION_SNAPPOINT_MANDATORY","directmanipulation/DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE","directmanipulation/DIRECTMANIPULATION_SNAPPOINT_OPTIONAL","directmanipulation/DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE","directmanipulation/DIRECTMANIPULATION_SNAPPOINT_TYPE"]
old-location: directmanipulation\directmanipulation_snappoint_type.htm
tech.root: directmanipulation
ms.assetid: 4ba8c216-a5bb-409d-bce8-fc85023b63d9
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_SNAPPOINT_MANDATORY, DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE, DIRECTMANIPULATION_SNAPPOINT_OPTIONAL, DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE, DIRECTMANIPULATION_SNAPPOINT_TYPE, DIRECTMANIPULATION_SNAPPOINT_TYPE enumeration [Direct Manipulation], directmanipulation.directmanipulation_snappoint_type, directmanipulation/DIRECTMANIPULATION_SNAPPOINT_MANDATORY, directmanipulation/DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE, directmanipulation/DIRECTMANIPULATION_SNAPPOINT_OPTIONAL, directmanipulation/DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE, directmanipulation/DIRECTMANIPULATION_SNAPPOINT_TYPE
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
req.typenames: DIRECTMANIPULATION_SNAPPOINT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_SNAPPOINT_TYPE
 - directmanipulation/DIRECTMANIPULATION_SNAPPOINT_TYPE
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
 - DIRECTMANIPULATION_SNAPPOINT_TYPE
---

# DIRECTMANIPULATION_SNAPPOINT_TYPE enumeration


## -description

Modifies how the final inertia end position is calculated.

## -enum-fields

### -field DIRECTMANIPULATION_SNAPPOINT_MANDATORY:0

Content always stops at the snap point closest to where inertia would naturally stop along the direction of inertia.

### -field DIRECTMANIPULATION_SNAPPOINT_OPTIONAL:1

Content stops at a snap point closest to where inertia would naturally stop along the direction of inertia, depending on how close the snap point is.

### -field DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE:2

Content always stops at the snap point closest to the release point along the direction of inertia.

### -field DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE:3

Content stops at the next snap point, if the motion starts far from it.

## -remarks

For <b>DIRECTMANIPULATION_SNAPPOINT_MANDATORY</b> or <b>DIRECTMANIPULATION_SNAPPOINT_OPTIONAL</b> snap points, the snap points are chosen based on the natural ending position of inertia as calculated by the touch interaction engine. For <b>DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE</b> or <b>DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE</b> snap points, the selected snap point depends on where inertia started.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
