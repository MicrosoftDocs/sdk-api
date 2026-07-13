---
UID: NE:inked.InkMode
title: InkMode (inked.h)
description: Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected.
helpviewer_keywords: ["81aac302-c89a-42ca-9c90-170611a8995a","IM_Disabled","IM_Ink","IM_InkAndGesture","InkMode","InkMode enumeration [Tablet PC]","inked/IM_Disabled","inked/IM_Ink","inked/IM_InkAndGesture","inked/InkMode","tablet.inkmode"]
old-location: tablet\inkmode.htm
tech.root: tablet
ms.assetid: 81aac302-c89a-42ca-9c90-170611a8995a
ms.date: 12/05/2018
ms.keywords: 81aac302-c89a-42ca-9c90-170611a8995a, IM_Disabled, IM_Ink, IM_InkAndGesture, InkMode, InkMode enumeration [Tablet PC], inked/IM_Disabled, inked/IM_Ink, inked/IM_InkAndGesture, inked/InkMode, tablet.inkmode
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: InkMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkMode
 - inked/InkMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - InkMode
---

## -description

Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected.

## -enum-fields

### -field IEM_Disabled:0

Ink collection is disabled. No strokes are created when in this mode.

### -field IEM_Ink:1

Ink only is collected, creating a stroke.

### -field IEM_InkAndGesture:2

Default. Ink is collected and single-stroke gestures are accepted.

## -see-also

<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit Control Reference</a>

<a href="/windows/desktop/tablet/inkedit-messages--win32-only-">InkEdit Messages</a>

<a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode">InkEdit::InkMode Property</a>
