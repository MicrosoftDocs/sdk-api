---
UID: NS:winuser.tagPOINTER_TYPE_INFO
title: POINTER_TYPE_INFO (winuser.h)
description: Contains information about the pointer input type.
helpviewer_keywords: ["*PPOINTER_TYPE_INFO","POINTER_TYPE_INFO","POINTER_TYPE_INFO structure","PPOINTER_TYPE_INFO","PPOINTER_TYPE_INFO structure pointer","input_pointerdevice.pointer_type_info","winuser/POINTER_TYPE_INFO","winuser/PPOINTER_TYPE_INFO"]
old-location: input_pointerdevice\pointer_type_info.htm
tech.root: controls
ms.assetid: 5EA8012C-CF0C-4771-9A9C-A9DC218DC9AB
ms.date: 12/05/2018
ms.keywords: '*PPOINTER_TYPE_INFO, POINTER_TYPE_INFO, POINTER_TYPE_INFO structure, PPOINTER_TYPE_INFO, PPOINTER_TYPE_INFO structure pointer, input_pointerdevice.pointer_type_info, winuser/POINTER_TYPE_INFO, winuser/PPOINTER_TYPE_INFO'
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: POINTER_TYPE_INFO, *PPOINTER_TYPE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_TYPE_INFO
 - winuser/tagPOINTER_TYPE_INFO
 - PPOINTER_TYPE_INFO
 - winuser/PPOINTER_TYPE_INFO
 - POINTER_TYPE_INFO
 - winuser/POINTER_TYPE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - POINTER_TYPE_INFO
---

# POINTER_TYPE_INFO structure


## -description

Contains information about the  pointer input type.

## -struct-fields

### -field type

The pointer input device.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.touchInfo

A [POINTER_TOUCH_INFO](ns-winuser-pointer_touch_info.md) structure representing basic touch information common to all pointer types.

### -field DUMMYUNIONNAME.penInfo

A [POINTER_PEN_INFO](ns-winuser-pointer_pen_info.md) structure representing basic pen information common to all pointer types.

