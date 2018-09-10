---
UID: NE:winuser.tagPOINTER_INPUT_TYPE
title: tagPOINTER_INPUT_TYPE
author: windows-sdk-content
description: Identifies the pointer input types.
old-location: inputmsg\pointer_input_type_enum.htm
tech.root: InputMsg
ms.assetid: 3334DCD0-DAE1-4AC2-AB36-23D114803100
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: POINTER_INPUT_TYPE, POINTER_INPUT_TYPE enumeration [Input Messages and Notifications], PT_MOUSE, PT_PEN, PT_POINTER, PT_TOUCH, PT_TOUCHPAD, inputmsg.pointer_input_type_enum, tagPOINTER_INPUT_TYPE, tagPOINTER_INPUT_TYPE enumeration [Input Messages and Notifications], winuser/PT_MOUSE, winuser/PT_PEN, winuser/PT_POINTER, winuser/PT_TOUCH, winuser/PT_TOUCHPAD, winuser/tagPOINTER_INPUT_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - POINTER_INPUT_TYPE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# tagPOINTER_INPUT_TYPE enumeration


## -description


Identifies the  pointer input types.


## -enum-fields




### -field PT_POINTER

Generic pointer type. This type never appears in pointer messages or pointer data. Some data query functions allow the caller to restrict the query to specific pointer type. The <b>PT_POINTER</b> type can be used in these functions to specify that the query is to include pointers of all types


### -field PT_TOUCH

Touch pointer type.


### -field PT_PEN

Pen pointer type.


### -field PT_MOUSE

Mouse pointer type.


### -field PT_TOUCHPAD

Touchpad pointer type (Windows 8.1 and later).


## -see-also




<a href="https://msdn.microsoft.com/22241CD0-DAE1-4AC2-AB36-23D114803133">Enumerations</a>
 

 

