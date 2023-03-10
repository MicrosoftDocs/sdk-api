---
UID: NE:tabflicks.KEYMODIFIER
title: KEYMODIFIER (tabflicks.h)
description: Determines which, if any, modifier keys were pressed when the flick gesture occurred.
helpviewer_keywords: ["KEYMODIFIER","KEYMODIFIER enumeration [Tablet PC]","KEYMODIFIER_ALTGR","KEYMODIFIER_CONTROL","KEYMODIFIER_EXT","KEYMODIFIER_MENU","KEYMODIFIER_SHIFT","KEYMODIFIER_WIN","ffb27356-9ad2-4759-bdc4-1025813a7258","tabflicks/KEYMODIFIER","tabflicks/KEYMODIFIER_ALTGR","tabflicks/KEYMODIFIER_CONTROL","tabflicks/KEYMODIFIER_EXT","tabflicks/KEYMODIFIER_MENU","tabflicks/KEYMODIFIER_SHIFT","tabflicks/KEYMODIFIER_WIN","tablet.keymodifier"]
old-location: tablet\keymodifier.htm
tech.root: tablet
ms.assetid: ffb27356-9ad2-4759-bdc4-1025813a7258
ms.date: 12/05/2018
ms.keywords: KEYMODIFIER, KEYMODIFIER enumeration [Tablet PC], KEYMODIFIER_ALTGR, KEYMODIFIER_CONTROL, KEYMODIFIER_EXT, KEYMODIFIER_MENU, KEYMODIFIER_SHIFT, KEYMODIFIER_WIN, ffb27356-9ad2-4759-bdc4-1025813a7258, tabflicks/KEYMODIFIER, tabflicks/KEYMODIFIER_ALTGR, tabflicks/KEYMODIFIER_CONTROL, tabflicks/KEYMODIFIER_EXT, tabflicks/KEYMODIFIER_MENU, tabflicks/KEYMODIFIER_SHIFT, tabflicks/KEYMODIFIER_WIN, tablet.keymodifier
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
req.typenames: KEYMODIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KEYMODIFIER
 - tabflicks/KEYMODIFIER
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
 - KEYMODIFIER
---

# KEYMODIFIER enumeration


## -description

Determines which, if any, modifier keys were pressed when the flick gesture occurred.

## -enum-fields

### -field KEYMODIFIER_CONTROL:1

The Control key was pressed when the Flicks gesture occurred.

### -field KEYMODIFIER_MENU:2

The Menu key was pressed when the Flicks gesture occurred.

### -field KEYMODIFIER_SHIFT:4

The Shift key was pressed when the Flicks gesture occurred.

### -field KEYMODIFIER_WIN:8

The Windows key was pressed when the Flicks gesture occurred.

### -field KEYMODIFIER_ALTGR:16

The Alt key was pressed when the Flicks gesture occurred.

### -field KEYMODIFIER_EXT:32

The pressed key's scan code was preceded by a prefix byte that has the value 0xE0 (224).

