---
UID: NE:winuser.tagPOINTER_INPUT_TYPE
title: tagPOINTER_INPUT_TYPE (winuser.h)
description: Identifies the pointer input types.
helpviewer_keywords: ["POINTER_INPUT_TYPE","POINTER_INPUT_TYPE enumeration [Input Messages and Notifications]","PT_MOUSE","PT_PEN","PT_POINTER","PT_TOUCH","PT_TOUCHPAD","inputmsg.pointer_input_type_enum","tagPOINTER_INPUT_TYPE","tagPOINTER_INPUT_TYPE enumeration [Input Messages and Notifications]","winuser/PT_MOUSE","winuser/PT_PEN","winuser/PT_POINTER","winuser/PT_TOUCH","winuser/PT_TOUCHPAD","winuser/tagPOINTER_INPUT_TYPE"]
old-location: inputmsg\pointer_input_type_enum.htm
tech.root: InputMsg
ms.assetid: 3334DCD0-DAE1-4AC2-AB36-23D114803100
ms.date: 12/05/2018
ms.keywords: POINTER_INPUT_TYPE, POINTER_INPUT_TYPE enumeration [Input Messages and Notifications], PT_MOUSE, PT_PEN, PT_POINTER, PT_TOUCH, PT_TOUCHPAD, inputmsg.pointer_input_type_enum, tagPOINTER_INPUT_TYPE, tagPOINTER_INPUT_TYPE enumeration [Input Messages and Notifications], winuser/PT_MOUSE, winuser/PT_PEN, winuser/PT_POINTER, winuser/PT_TOUCH, winuser/PT_TOUCHPAD, winuser/tagPOINTER_INPUT_TYPE
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_INPUT_TYPE
 - winuser/tagPOINTER_INPUT_TYPE
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
 - POINTER_INPUT_TYPE
---

# tagPOINTER_INPUT_TYPE enumeration


## -description

Identifies the  pointer input types.

## -enum-fields

### -field PT_POINTER:1

Generic pointer type. This type never appears in pointer messages or pointer data. Some data query functions allow the caller to restrict the query to specific pointer type. The <b>PT_POINTER</b> type can be used in these functions to specify that the query is to include pointers of all types

### -field PT_TOUCH:2

Touch pointer type.

### -field PT_PEN:3

Pen pointer type.

### -field PT_MOUSE:4

Mouse pointer type.

### -field PT_TOUCHPAD:5

Touchpad pointer type (Windows 8.1 and later).

## -see-also

<a href="/previous-versions/windows/desktop/inputmsg/enums">Enumerations</a>
