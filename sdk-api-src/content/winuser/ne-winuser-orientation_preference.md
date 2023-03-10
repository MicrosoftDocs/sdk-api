---
UID: NE:winuser.ORIENTATION_PREFERENCE
title: ORIENTATION_PREFERENCE (winuser.h)
description: Indicates the screen orientation preference for a desktop app process.
helpviewer_keywords: ["ORIENTATION_PREFERENCE","ORIENTATION_PREFERENCE enumeration","ORIENTATION_PREFERENCE_LANDSCAPE","ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED","ORIENTATION_PREFERENCE_NONE","ORIENTATION_PREFERENCE_PORTRAIT","ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED","base.orientation_preference","winuser/ORIENTATION_PREFERENCE","winuser/ORIENTATION_PREFERENCE_LANDSCAPE","winuser/ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED","winuser/ORIENTATION_PREFERENCE_NONE","winuser/ORIENTATION_PREFERENCE_PORTRAIT","winuser/ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED"]
old-location: base\orientation_preference.htm
tech.root: backup
ms.assetid: 7399DD9F-F993-40CC-B9C6-20673D39C069
ms.date: 12/05/2018
ms.keywords: ORIENTATION_PREFERENCE, ORIENTATION_PREFERENCE enumeration, ORIENTATION_PREFERENCE_LANDSCAPE, ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED, ORIENTATION_PREFERENCE_NONE, ORIENTATION_PREFERENCE_PORTRAIT, ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED, base.orientation_preference, winuser/ORIENTATION_PREFERENCE, winuser/ORIENTATION_PREFERENCE_LANDSCAPE, winuser/ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED, winuser/ORIENTATION_PREFERENCE_NONE, winuser/ORIENTATION_PREFERENCE_PORTRAIT, winuser/ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: ORIENTATION_PREFERENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ORIENTATION_PREFERENCE
 - winuser/ORIENTATION_PREFERENCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinUser.h
api_name:
 - ORIENTATION_PREFERENCE
---

# ORIENTATION_PREFERENCE enumeration


## -description

Indicates the screen orientation preference for a desktop app process.

## -enum-fields

### -field ORIENTATION_PREFERENCE_NONE:0x0

The process has no device orientation preferences. The system may choose any available setting.

### -field ORIENTATION_PREFERENCE_LANDSCAPE:0x1

The process represents a desktop app that can be used in landscape mode.

### -field ORIENTATION_PREFERENCE_PORTRAIT:0x2

The process represents a desktop app that can be used in portrait mode.

### -field ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED:0x4

 The process represents a desktop app that can be used in flipped landscape mode.

### -field ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED:0x8

The process represents a desktop app that can be used in flipped portrait mode.

