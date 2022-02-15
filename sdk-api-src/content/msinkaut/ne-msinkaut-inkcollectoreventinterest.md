---
UID: NE:msinkaut.InkCollectorEventInterest
title: InkCollectorEventInterest (msinkaut.h)
description: Defines values that are used to specify whether an event occurred on an ink collector and, if so, which event fired.
helpviewer_keywords: ["ICEI_AllEvents","ICEI_CursorButtonDown","ICEI_CursorButtonUp","ICEI_CursorDown","ICEI_CursorInRange","ICEI_CursorOutOfRange","ICEI_DblClick","ICEI_DefaultEvents","ICEI_MouseDown","ICEI_MouseMove","ICEI_MouseUp","ICEI_MouseWheel","ICEI_NewInAirPackets","ICEI_NewPackets","ICEI_Stroke","ICEI_SystemGesture","ICEI_TabletAdded","ICEI_TabletRemoved","InkCollectorEventInterest","InkCollectorEventInterest enumeration [Tablet PC]","db575790-345b-48da-b509-927eb2f47987","msinkaut/ICEI_AllEvents","msinkaut/ICEI_CursorButtonDown","msinkaut/ICEI_CursorButtonUp","msinkaut/ICEI_CursorDown","msinkaut/ICEI_CursorInRange","msinkaut/ICEI_CursorOutOfRange","msinkaut/ICEI_DblClick","msinkaut/ICEI_DefaultEvents","msinkaut/ICEI_MouseDown","msinkaut/ICEI_MouseMove","msinkaut/ICEI_MouseUp","msinkaut/ICEI_MouseWheel","msinkaut/ICEI_NewInAirPackets","msinkaut/ICEI_NewPackets","msinkaut/ICEI_Stroke","msinkaut/ICEI_SystemGesture","msinkaut/ICEI_TabletAdded","msinkaut/ICEI_TabletRemoved","msinkaut/InkCollectorEventInterest","tablet.inkcollectoreventinterest"]
old-location: tablet\inkcollectoreventinterest.htm
tech.root: tablet
ms.assetid: db575790-345b-48da-b509-927eb2f47987
ms.date: 12/05/2018
ms.keywords: ICEI_AllEvents, ICEI_CursorButtonDown, ICEI_CursorButtonUp, ICEI_CursorDown, ICEI_CursorInRange, ICEI_CursorOutOfRange, ICEI_DblClick, ICEI_DefaultEvents, ICEI_MouseDown, ICEI_MouseMove, ICEI_MouseUp, ICEI_MouseWheel, ICEI_NewInAirPackets, ICEI_NewPackets, ICEI_Stroke, ICEI_SystemGesture, ICEI_TabletAdded, ICEI_TabletRemoved, InkCollectorEventInterest, InkCollectorEventInterest enumeration [Tablet PC], db575790-345b-48da-b509-927eb2f47987, msinkaut/ICEI_AllEvents, msinkaut/ICEI_CursorButtonDown, msinkaut/ICEI_CursorButtonUp, msinkaut/ICEI_CursorDown, msinkaut/ICEI_CursorInRange, msinkaut/ICEI_CursorOutOfRange, msinkaut/ICEI_DblClick, msinkaut/ICEI_DefaultEvents, msinkaut/ICEI_MouseDown, msinkaut/ICEI_MouseMove, msinkaut/ICEI_MouseUp, msinkaut/ICEI_MouseWheel, msinkaut/ICEI_NewInAirPackets, msinkaut/ICEI_NewPackets, msinkaut/ICEI_Stroke, msinkaut/ICEI_SystemGesture, msinkaut/ICEI_TabletAdded, msinkaut/ICEI_TabletRemoved, msinkaut/InkCollectorEventInterest, tablet.inkcollectoreventinterest
req.header: msinkaut.h
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
req.typenames: InkCollectorEventInterest
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkCollectorEventInterest
 - msinkaut/InkCollectorEventInterest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkCollectorEventInterest
---

# InkCollectorEventInterest enumeration


## -description

Defines values that are used to specify whether an event occurred on an ink collector and, if so, which event fired. To get the status of a given event, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest">GetEventInterest</a> method. To set the status of a given event, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest">SetEventInterest</a> method.

## -enum-fields

### -field ICEI_DefaultEvents:-1

The ink collector is interested in the <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a>, <a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a>, and <a href="/windows/desktop/tablet/inkcollector-cursoroutofrange">CursorOutOfRange</a> events.

### -field ICEI_CursorDown

The ink collector detects a cursor down.

### -field ICEI_Stroke

Specifies that a new stroke is drawn on a tablet.

### -field ICEI_NewPackets

The ink collector receives a <i>packet</i>.

### -field ICEI_NewInAirPackets

The ink collector detects an in-air packet.

### -field ICEI_CursorButtonDown

The ink collector detects a cursor button down.

### -field ICEI_CursorButtonUp

The ink collector detects a cursor button up.

### -field ICEI_CursorInRange

Specifies that a cursor is detected in range of a tablet.

### -field ICEI_CursorOutOfRange

Specifies that a cursor is detected leaving the range of a tablet.

### -field ICEI_SystemGesture

The ink collector recognizes a system gesture.

### -field ICEI_TabletAdded

Specifies that a tablet was added to the system.

### -field ICEI_TabletRemoved

Specifies that a tablet was removed from the system.

### -field ICEI_MouseDown

The mouse pointer is over the object and a mouse button is pressed.

### -field ICEI_MouseMove

The mouse pointer is moved over the object.

### -field ICEI_MouseUp

The mouse pointer is over the object and a mouse button is released.

### -field ICEI_MouseWheel

The mouse wheel moves while the object has focus.

### -field ICEI_DblClick

The object was double-clicked.

### -field ICEI_AllEvents

The ink collector recognizes all events.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest">GetEventInterest Method</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest">SetEventInterest Method</a>
