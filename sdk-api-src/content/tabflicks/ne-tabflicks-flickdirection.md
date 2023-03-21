---
UID: NE:tabflicks.FLICKDIRECTION
title: FLICKDIRECTION (tabflicks.h)
description: Defines the directions in which a pen flick has occurred.
helpviewer_keywords: ["49b282cb-45e6-4f80-9948-fd736c091e70","FLICKDIRECTION","FLICKDIRECTION enumeration [Tablet PC]","FLICKDIRECTION_DOWN","FLICKDIRECTION_DOWNLEFT","FLICKDIRECTION_DOWNRIGHT","FLICKDIRECTION_INVALID","FLICKDIRECTION_LEFT","FLICKDIRECTION_RIGHT","FLICKDIRECTION_UP","FLICKDIRECTION_UPLEFT","FLICKDIRECTION_UPRIGHT","tabflicks/FLICKDIRECTION","tabflicks/FLICKDIRECTION_DOWN","tabflicks/FLICKDIRECTION_DOWNLEFT","tabflicks/FLICKDIRECTION_DOWNRIGHT","tabflicks/FLICKDIRECTION_INVALID","tabflicks/FLICKDIRECTION_LEFT","tabflicks/FLICKDIRECTION_RIGHT","tabflicks/FLICKDIRECTION_UP","tabflicks/FLICKDIRECTION_UPLEFT","tabflicks/FLICKDIRECTION_UPRIGHT","tablet.flickdirection"]
old-location: tablet\flickdirection.htm
tech.root: tablet
ms.assetid: 49b282cb-45e6-4f80-9948-fd736c091e70
ms.date: 12/05/2018
ms.keywords: 49b282cb-45e6-4f80-9948-fd736c091e70, FLICKDIRECTION, FLICKDIRECTION enumeration [Tablet PC], FLICKDIRECTION_DOWN, FLICKDIRECTION_DOWNLEFT, FLICKDIRECTION_DOWNRIGHT, FLICKDIRECTION_INVALID, FLICKDIRECTION_LEFT, FLICKDIRECTION_RIGHT, FLICKDIRECTION_UP, FLICKDIRECTION_UPLEFT, FLICKDIRECTION_UPRIGHT, tabflicks/FLICKDIRECTION, tabflicks/FLICKDIRECTION_DOWN, tabflicks/FLICKDIRECTION_DOWNLEFT, tabflicks/FLICKDIRECTION_DOWNRIGHT, tabflicks/FLICKDIRECTION_INVALID, tabflicks/FLICKDIRECTION_LEFT, tabflicks/FLICKDIRECTION_RIGHT, tabflicks/FLICKDIRECTION_UP, tabflicks/FLICKDIRECTION_UPLEFT, tabflicks/FLICKDIRECTION_UPRIGHT, tablet.flickdirection
req.header: tabflicks.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FLICKDIRECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FLICKDIRECTION
 - tabflicks/FLICKDIRECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tabflicks.h
api_name:
 - FLICKDIRECTION
---

# FLICKDIRECTION enumeration


## -description

Defines the directions in which a pen flick has occurred.

## -enum-fields

### -field FLICKDIRECTION_MIN:0

### -field FLICKDIRECTION_RIGHT:0

 A pen flick to the right.

### -field FLICKDIRECTION_UPRIGHT:1

 A pen flick to the upper right.

### -field FLICKDIRECTION_UP:2

 An upward pen flick.

### -field FLICKDIRECTION_UPLEFT:3

A pen flick to the upper left.

### -field FLICKDIRECTION_LEFT:4

A pen flick to the left.

### -field FLICKDIRECTION_DOWNLEFT:5

A pen flick to the lower left.

### -field FLICKDIRECTION_DOWN:6

A downward pen flick.

### -field FLICKDIRECTION_DOWNRIGHT:7

A pen flick to the down right.

### -field FLICKDIRECTION_INVALID:8

An invalid pen flick.

## -remarks

A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion. A flick is characterized by high speed and a high degree of straightness. A flick is identified by its direction. Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.

## -see-also

<a href="/windows/desktop/api/tabflicks/ns-tabflicks-flick_data">FLICK_DATA Structure</a>



<a href="/windows/desktop/tablet/flicks-gestures">Flicks Gestures</a>



<a href="/previous-versions/windows/desktop/ms703447(v=vs.85)">Responding to Pen Flicks</a>



<a href="/windows/desktop/tablet/wm-tablet-flick-message">WM_TABLET_FLICK Message</a>
