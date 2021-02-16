---
UID: NS:tpcshrd.tagSYSTEM_EVENT_DATA
title: SYSTEM_EVENT_DATA (tpcshrd.h)
description: Contains information about a tablet system event.
helpviewer_keywords: ["3a2c33b7-91ca-48eb-a5b9-a1ccb5106f90","SYSTEM_EVENT_DATA","SYSTEM_EVENT_DATA structure [Tablet PC]","tablet.system_event_data","tagSYSTEM_EVENT_DATA","tpcshrd/SYSTEM_EVENT_DATA"]
old-location: tablet\system_event_data.htm
tech.root: tablet
ms.assetid: 3a2c33b7-91ca-48eb-a5b9-a1ccb5106f90
ms.date: 12/05/2018
ms.keywords: 3a2c33b7-91ca-48eb-a5b9-a1ccb5106f90, SYSTEM_EVENT_DATA, SYSTEM_EVENT_DATA structure [Tablet PC], tablet.system_event_data, tagSYSTEM_EVENT_DATA, tpcshrd/SYSTEM_EVENT_DATA
req.header: tpcshrd.h
req.include-header: RTSCom.h
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
req.typenames: SYSTEM_EVENT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSYSTEM_EVENT_DATA
 - tpcshrd/tagSYSTEM_EVENT_DATA
 - SYSTEM_EVENT_DATA
 - tpcshrd/SYSTEM_EVENT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - SYSTEM_EVENT_DATA
---

# SYSTEM_EVENT_DATA structure


## -description

Contains information about a tablet system event.

## -struct-fields

### -field bModifier

Bit values for the modifiers. Possible values include SE_MODIFIER_CTRL (the Control key was pressed), SE_MODIFIER_ALT (the Alt key was pressed), and SE_MODIFIER_SHIFT (the Shift key was pressed).

### -field wKey

Scan code for the keyboard character.

### -field xPos

X position of the event.

### -field yPos

Y position of the event.

### -field bCursorMode

The type of cursor that caused the event. Possible values include SE_NORMAL_CURSOR (the pen tip) and SE_ERASER_CURSOR (the eraser).

### -field dwButtonState

State of the buttons at the time of the system event.

## -see-also

<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-systemevent">IStylusPlugin::SystemEvent Method</a>



<a href="/windows/desktop/tablet/itableteventsink-systemevent">ITabletEventSink::SystemEvent Method</a>