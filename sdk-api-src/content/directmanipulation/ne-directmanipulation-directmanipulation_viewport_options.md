---
UID: NE:directmanipulation.DIRECTMANIPULATION_VIEWPORT_OPTIONS
title: DIRECTMANIPULATION_VIEWPORT_OPTIONS (directmanipulation.h)
description: Defines the input behavior options for the viewport.
helpviewer_keywords: ["DIRECTMANIPULATION_VIEWPORT_OPTIONS","DIRECTMANIPULATION_VIEWPORT_OPTIONS enumeration [Direct Manipulation]","DIRECTMANIPULATION_VIEWPORT_OPTIONS_AUTODISABLE","DIRECTMANIPULATION_VIEWPORT_OPTIONS_DEFAULT","DIRECTMANIPULATION_VIEWPORT_OPTIONS_DISABLEPIXELSNAPPING","DIRECTMANIPULATION_VIEWPORT_OPTIONS_EXPLICITHITTEST","DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT","DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE","directmanipulation.directmanipulation_viewport_options","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_AUTODISABLE","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_DEFAULT","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_DISABLEPIXELSNAPPING","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_EXPLICITHITTEST","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT","directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE"]
old-location: directmanipulation\directmanipulation_viewport_options.htm
tech.root: directmanipulation
ms.assetid: BFBA2D32-825F-4EEF-99C8-291305926750
ms.date: 12/05/2018
ms.keywords: DIRECTMANIPULATION_VIEWPORT_OPTIONS, DIRECTMANIPULATION_VIEWPORT_OPTIONS enumeration [Direct Manipulation], DIRECTMANIPULATION_VIEWPORT_OPTIONS_AUTODISABLE, DIRECTMANIPULATION_VIEWPORT_OPTIONS_DEFAULT, DIRECTMANIPULATION_VIEWPORT_OPTIONS_DISABLEPIXELSNAPPING, DIRECTMANIPULATION_VIEWPORT_OPTIONS_EXPLICITHITTEST, DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT, DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE, directmanipulation.directmanipulation_viewport_options, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_AUTODISABLE, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_DEFAULT, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_DISABLEPIXELSNAPPING, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_EXPLICITHITTEST, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT, directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTMANIPULATION_VIEWPORT_OPTIONS
 - directmanipulation/DIRECTMANIPULATION_VIEWPORT_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directmanipulation.h
api_name:
 - DIRECTMANIPULATION_VIEWPORT_OPTIONS
---

# DIRECTMANIPULATION_VIEWPORT_OPTIONS enumeration


## -description

Defines the input behavior options for the viewport.

## -enum-fields

### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_DEFAULT:0

No special behaviors. This is the default value used to set or revert to default behavior.

### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_AUTODISABLE:0x1

At the end of an interaction, the viewport transitions to <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_status">DIRECTMANIPULATION_READY</a> and then immediately to <b>DIRECTMANIPULATION_DISABLED</b>. The viewport must be explicitly enabled through the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-enable">Enable</a> method before the next interaction can be processed.

### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE:0x2

<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-update">Update</a> must be called to redraw the content within the viewport. The content is not updated automatically during an input event.

### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_INPUT:0x4

All input from a contact associated with the viewport is passed to the UI thread for processing.

### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_EXPLICITHITTEST:0x8

If set, all <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerdown">WM_POINTERDOWN</a> messages are passed to the application for hit testing. Otherwise, <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> will process the messages for hit testing against the existing list of running viewports, and the application will not see the input.

Applies only when viewport state is <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_status">DIRECTMANIPULATION_RUNNING</a> or <b>DIRECTMANIPULATION_INERTIA</b>.

### -field DIRECTMANIPULATION_VIEWPORT_OPTIONS_DISABLEPIXELSNAPPING:0x10

Specifies that pixel snapping during a manipulation is disabled.

Anti-aliasing can create irregular edge rendering. Artifacts, commonly seen as blurry, or semi-transparent, edges can occur when the location of an edge falls in the middle of a device pixel rather than between device pixels.

## -remarks

<b>DIRECTMANIPULATION_VIEWPORT_OPTIONS</b> is used in the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportoptions">SetViewportOptions</a> method. These flags can be combined to set the input behavior for a viewport.

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-enumerations">Direct Manipulation Enumerations</a>
