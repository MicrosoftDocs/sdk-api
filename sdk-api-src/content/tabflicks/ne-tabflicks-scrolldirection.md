---
UID: NE:tabflicks.SCROLLDIRECTION
title: SCROLLDIRECTION (tabflicks.h)
description: Defines the direction of the scrolling command for a pen flick.
helpviewer_keywords: ["79d64632-a0ac-4c1b-83e3-76c9fbd11da9","SCROLLDIRECTION","SCROLLDIRECTION enumeration [Tablet PC]","SCROLLDIRECTION_DOWN","SCROLLDIRECTION_UP","tabflicks/SCROLLDIRECTION","tabflicks/SCROLLDIRECTION_DOWN","tabflicks/SCROLLDIRECTION_UP","tablet.scrolldirection"]
old-location: tablet\scrolldirection.htm
tech.root: tablet
ms.assetid: 79d64632-a0ac-4c1b-83e3-76c9fbd11da9
ms.date: 12/05/2018
ms.keywords: 79d64632-a0ac-4c1b-83e3-76c9fbd11da9, SCROLLDIRECTION, SCROLLDIRECTION enumeration [Tablet PC], SCROLLDIRECTION_DOWN, SCROLLDIRECTION_UP, tabflicks/SCROLLDIRECTION, tabflicks/SCROLLDIRECTION_DOWN, tabflicks/SCROLLDIRECTION_UP, tablet.scrolldirection
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
req.typenames: SCROLLDIRECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCROLLDIRECTION
 - tabflicks/SCROLLDIRECTION
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
 - SCROLLDIRECTION
---

# SCROLLDIRECTION enumeration


## -description

Defines the direction of the scrolling command for a pen flick.

## -enum-fields

### -field SCROLLDIRECTION_UP:0

 The flick action is a Scroll Up command.

### -field SCROLLDIRECTION_DOWN:1

The flick action is a Scroll Down command.

## -remarks

When the user performs a pen flick that is assigned to a scrolling command, the <a href="/windows/desktop/tablet/wm-tablet-flick-message">WM_TABLET_FLICK Message</a> sends the direction of the scrolling command as part of the <a href="/windows/desktop/api/tabflicks/ns-tabflicks-flick_data">FLICK_DATA Structure</a>.

## -see-also

<a href="/windows/desktop/api/tabflicks/ns-tabflicks-flick_data">flick_data structure</a>



<a href="/windows/desktop/tablet/flicks-gestures">flicks gestures</a>



<a href="/previous-versions/windows/desktop/ms703447(v=vs.85)">responding to pen flicks</a>



<a href="/windows/desktop/tablet/wm-tablet-flick-message">wm_tablet_flick message</a>
