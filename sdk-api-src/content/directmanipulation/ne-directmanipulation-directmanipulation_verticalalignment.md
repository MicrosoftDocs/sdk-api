---
UID: NE:directmanipulation.DIRECTMANIPULATION_VERTICALALIGNMENT
title: DIRECTMANIPULATION_VERTICALALIGNMENT (directmanipulation.h)
description: Defines the vertical alignment settings for content within the viewport.
helpviewer_keywords: ["DIRECTMANIPULATION_VERTICALALIGNMENT","DIRECTMANIPULATION_VERTICALALIGNMENT enumeration [Direct Manipulation]","DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM","DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER","DIRECTMANIPULATION_VERTICALALIGNMENT_NONE","DIRECTMANIPULATION_VERTICALALIGNMENT_TOP","DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER","directmanipulation.directmanipulation_verticalalignment","directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT","directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM","directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER","directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_NONE","directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_TOP","directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER"]
old-location: directmanipulation\directmanipulation_verticalalignment.htm
tech.root: directmanipulation
ms.assetid: 37e9a604-f713-4203-928c-0799206b76fe
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_VERTICALALIGNMENT, DIRECTMANIPULATION_VERTICALALIGNMENT enumeration [Direct Manipulation], DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM, DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER, DIRECTMANIPULATION_VERTICALALIGNMENT_NONE, DIRECTMANIPULATION_VERTICALALIGNMENT_TOP, DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER, directmanipulation.directmanipulation_verticalalignment, directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT, directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM, directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER, directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_NONE, directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_TOP, directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER
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
req.typenames: DIRECTMANIPULATION_VERTICALALIGNMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_VERTICALALIGNMENT
 - directmanipulation/DIRECTMANIPULATION_VERTICALALIGNMENT
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
 - DIRECTMANIPULATION_VERTICALALIGNMENT
---

# DIRECTMANIPULATION_VERTICALALIGNMENT enumeration


## -description

Defines  the vertical alignment settings for content within the viewport.

## -enum-fields

### -field DIRECTMANIPULATION_VERTICALALIGNMENT_NONE:0

No alignment. The object can be positioned anywhere within the viewport.

### -field DIRECTMANIPULATION_VERTICALALIGNMENT_TOP:0x1

Align object along the top of the viewport.

### -field DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER:0x2

Align object to the center of the viewport.

### -field DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM:0x4

Align object along the bottom of the viewport.

### -field DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER:0x8

Content zooms around the center point of the contacts, instead of being locked with the vertical alignment.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
