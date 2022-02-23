---
UID: NE:winuser.tagPOINTER_BUTTON_CHANGE_TYPE
title: POINTER_BUTTON_CHANGE_TYPE (winuser.h)
description: Identifies a change in the state of a button associated with a pointer.
helpviewer_keywords: ["POINTER_BUTTON_CHANGE_TYPE","POINTER_BUTTON_CHANGE_TYPE enumeration [Input Messages and Notifications]","POINTER_CHANGE_FIFTHBUTTON_DOWN","POINTER_CHANGE_FIFTHBUTTON_UP","POINTER_CHANGE_FIRSTBUTTON_DOWN","POINTER_CHANGE_FIRSTBUTTON_UP","POINTER_CHANGE_FOURTHBUTTON_DOWN","POINTER_CHANGE_FOURTHBUTTON_UP","POINTER_CHANGE_NONE","POINTER_CHANGE_SECONDBUTTON_DOWN","POINTER_CHANGE_SECONDBUTTON_UP","POINTER_CHANGE_THIRDBUTTON_DOWN","POINTER_CHANGE_THIRDBUTTON_UP","inputmsg.pointer_button_change_type","winuser/POINTER_BUTTON_CHANGE_TYPE","winuser/POINTER_CHANGE_FIFTHBUTTON_DOWN","winuser/POINTER_CHANGE_FIFTHBUTTON_UP","winuser/POINTER_CHANGE_FIRSTBUTTON_DOWN","winuser/POINTER_CHANGE_FIRSTBUTTON_UP","winuser/POINTER_CHANGE_FOURTHBUTTON_DOWN","winuser/POINTER_CHANGE_FOURTHBUTTON_UP","winuser/POINTER_CHANGE_NONE","winuser/POINTER_CHANGE_SECONDBUTTON_DOWN","winuser/POINTER_CHANGE_SECONDBUTTON_UP","winuser/POINTER_CHANGE_THIRDBUTTON_DOWN","winuser/POINTER_CHANGE_THIRDBUTTON_UP"]
old-location: inputmsg\pointer_button_change_type.htm
tech.root: InputMsg
ms.assetid: DF5F60F6-8FD9-41EB-AF2A-09A17513659C
ms.date: 12/05/2018
ms.keywords: POINTER_BUTTON_CHANGE_TYPE, POINTER_BUTTON_CHANGE_TYPE enumeration [Input Messages and Notifications], POINTER_CHANGE_FIFTHBUTTON_DOWN, POINTER_CHANGE_FIFTHBUTTON_UP, POINTER_CHANGE_FIRSTBUTTON_DOWN, POINTER_CHANGE_FIRSTBUTTON_UP, POINTER_CHANGE_FOURTHBUTTON_DOWN, POINTER_CHANGE_FOURTHBUTTON_UP, POINTER_CHANGE_NONE, POINTER_CHANGE_SECONDBUTTON_DOWN, POINTER_CHANGE_SECONDBUTTON_UP, POINTER_CHANGE_THIRDBUTTON_DOWN, POINTER_CHANGE_THIRDBUTTON_UP, inputmsg.pointer_button_change_type, winuser/POINTER_BUTTON_CHANGE_TYPE, winuser/POINTER_CHANGE_FIFTHBUTTON_DOWN, winuser/POINTER_CHANGE_FIFTHBUTTON_UP, winuser/POINTER_CHANGE_FIRSTBUTTON_DOWN, winuser/POINTER_CHANGE_FIRSTBUTTON_UP, winuser/POINTER_CHANGE_FOURTHBUTTON_DOWN, winuser/POINTER_CHANGE_FOURTHBUTTON_UP, winuser/POINTER_CHANGE_NONE, winuser/POINTER_CHANGE_SECONDBUTTON_DOWN, winuser/POINTER_CHANGE_SECONDBUTTON_UP, winuser/POINTER_CHANGE_THIRDBUTTON_DOWN, winuser/POINTER_CHANGE_THIRDBUTTON_UP
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
req.typenames: POINTER_BUTTON_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTER_BUTTON_CHANGE_TYPE
 - winuser/tagPOINTER_BUTTON_CHANGE_TYPE
 - POINTER_BUTTON_CHANGE_TYPE
 - winuser/POINTER_BUTTON_CHANGE_TYPE
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
 - POINTER_BUTTON_CHANGE_TYPE
---

# POINTER_BUTTON_CHANGE_TYPE enumeration


## -description

Identifies a change in the state of a button associated with a pointer.

## -enum-fields

### -field POINTER_CHANGE_NONE

No change in button state.

### -field POINTER_CHANGE_FIRSTBUTTON_DOWN

The first button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_FIRSTBUTTON</a>) transitioned to a pressed state.

### -field POINTER_CHANGE_FIRSTBUTTON_UP

The first button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_FIRSTBUTTON</a>) transitioned to a released state.

### -field POINTER_CHANGE_SECONDBUTTON_DOWN

The second button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_SECONDBUTTON</a>) transitioned to a pressed state.

### -field POINTER_CHANGE_SECONDBUTTON_UP

The second button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_SECONDBUTTON</a>) transitioned to a released state.

### -field POINTER_CHANGE_THIRDBUTTON_DOWN

The third button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_THIRDBUTTON</a>) transitioned to a pressed state.

### -field POINTER_CHANGE_THIRDBUTTON_UP

The third button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_THIRDBUTTON</a>) transitioned to a released state.

### -field POINTER_CHANGE_FOURTHBUTTON_DOWN

The fourth button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_FOURTHBUTTON</a>) transitioned to a pressed state.

### -field POINTER_CHANGE_FOURTHBUTTON_UP

The fourth button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_FOURTHBUTTON</a>) transitioned to a released state.

### -field POINTER_CHANGE_FIFTHBUTTON_DOWN

The fifth button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_FIFTHBUTTON</a>) transitioned to a pressed state.

### -field POINTER_CHANGE_FIFTHBUTTON_UP

The fifth button (see <a href="/windows/win32/inputmsg/pointer-flags-contants">POINTER_FLAG_FIFTHBUTTON</a>) transitioned to a released state.

## -see-also

<a href="/windows/win32/inputmsg/enums">Enumerations</a>



<a href="/windows/desktop/api/winuser/ns-winuser-pointer_info">POINTER_INFO</a>