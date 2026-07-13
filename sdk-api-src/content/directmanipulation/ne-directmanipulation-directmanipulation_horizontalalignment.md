---
UID: NE:directmanipulation.DIRECTMANIPULATION_HORIZONTALALIGNMENT
title: DIRECTMANIPULATION_HORIZONTALALIGNMENT (directmanipulation.h)
description: Defines the horizontal alignment options for content within a viewport.
helpviewer_keywords: ["DIRECTMANIPULATION_HORIZONTALALIGNMENT","DIRECTMANIPULATION_HORIZONTALALIGNMENT enumeration [Direct Manipulation]","DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER","DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT","DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE","DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT","DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER","directmanipulation.directmanipulation_horizontalalignment","directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT","directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER","directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT","directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE","directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT","directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER"]
old-location: directmanipulation\directmanipulation_horizontalalignment.htm
tech.root: directmanipulation
ms.assetid: ced17ad6-0728-46ed-8c04-d0c588f0bb38
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_HORIZONTALALIGNMENT, DIRECTMANIPULATION_HORIZONTALALIGNMENT enumeration [Direct Manipulation], DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER, DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT, DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE, DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT, DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER, directmanipulation.directmanipulation_horizontalalignment, directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT, directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER, directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT, directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE, directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT, directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER
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
req.typenames: DIRECTMANIPULATION_HORIZONTALALIGNMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_HORIZONTALALIGNMENT
 - directmanipulation/DIRECTMANIPULATION_HORIZONTALALIGNMENT
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
 - DIRECTMANIPULATION_HORIZONTALALIGNMENT
---

# DIRECTMANIPULATION_HORIZONTALALIGNMENT enumeration


## -description

Defines the horizontal alignment options for content within a viewport.

## -enum-fields

### -field DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE:0

No alignment. The object can be positioned anywhere within the viewport.

### -field DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT:0x1

Align object along the left side of the viewport.

### -field DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER:0x2

Align object to the center of the viewport.

### -field DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT:0x4

Align object along the right side of the viewport.

### -field DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER:0x8

Content zooms around the center point of the contacts, instead of being locked with the horizontal alignment.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
