---
UID: NE:tabflicks.FLICKACTION_COMMANDCODE
title: FLICKACTION_COMMANDCODE (tabflicks.h)
description: Defines the possible flick actions that can be assigned to a pen flick.
helpviewer_keywords: ["FLICKACTION_COMMANDCODE","FLICKACTION_COMMANDCODE enumeration [Tablet PC]","FLICKACTION_COMMANDCODE_APPCOMMAND","FLICKACTION_COMMANDCODE_CUSTOMKEY","FLICKACTION_COMMANDCODE_KEYMODIFIER","FLICKACTION_COMMANDCODE_NULL","FLICKACTION_COMMANDCODE_SCROLL","cb923201-5205-494e-bb67-5a908cb570e5","tabflicks/FLICKACTION_COMMANDCODE","tabflicks/FLICKACTION_COMMANDCODE_APPCOMMAND","tabflicks/FLICKACTION_COMMANDCODE_CUSTOMKEY","tabflicks/FLICKACTION_COMMANDCODE_KEYMODIFIER","tabflicks/FLICKACTION_COMMANDCODE_NULL","tabflicks/FLICKACTION_COMMANDCODE_SCROLL","tablet.flickaction_commandmode"]
old-location: tablet\flickaction_commandmode.htm
tech.root: tablet
ms.assetid: cb923201-5205-494e-bb67-5a908cb570e5
ms.date: 12/05/2018
ms.keywords: FLICKACTION_COMMANDCODE, FLICKACTION_COMMANDCODE enumeration [Tablet PC], FLICKACTION_COMMANDCODE_APPCOMMAND, FLICKACTION_COMMANDCODE_CUSTOMKEY, FLICKACTION_COMMANDCODE_KEYMODIFIER, FLICKACTION_COMMANDCODE_NULL, FLICKACTION_COMMANDCODE_SCROLL, cb923201-5205-494e-bb67-5a908cb570e5, tabflicks/FLICKACTION_COMMANDCODE, tabflicks/FLICKACTION_COMMANDCODE_APPCOMMAND, tabflicks/FLICKACTION_COMMANDCODE_CUSTOMKEY, tabflicks/FLICKACTION_COMMANDCODE_KEYMODIFIER, tabflicks/FLICKACTION_COMMANDCODE_NULL, tabflicks/FLICKACTION_COMMANDCODE_SCROLL, tablet.flickaction_commandmode
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
req.typenames: FLICKACTION_COMMANDCODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FLICKACTION_COMMANDCODE
 - tabflicks/FLICKACTION_COMMANDCODE
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
 - FLICKACTION_COMMANDCODE
---

# FLICKACTION_COMMANDCODE enumeration


## -description

Defines the possible flick actions that can be assigned to a pen flick.

## -enum-fields

### -field FLICKACTION_COMMANDCODE_NULL:0

No action is assigned to the pen flick.

### -field FLICKACTION_COMMANDCODE_SCROLL:1

A scrolling command is assigned to the pen flick.

### -field FLICKACTION_COMMANDCODE_APPCOMMAND:2

An application command is assigned to a pen flick.

### -field FLICKACTION_COMMANDCODE_CUSTOMKEY:3

A customized key sequence is assigned to the pen flick.

### -field FLICKACTION_COMMANDCODE_KEYMODIFIER:4

A key modifier is assigned to the pen flick.

## -remarks

In Control Panel, the user can assign commands to pen flicks. Four types of actions with pen flicks include:

<ul>
<li>Scroll Up or Scroll Down.</li>
<li>An application command such as Back or Undo</li>
<li>Any keystroke or keystroke combination such as CONTROL+N.</li>
<li>Activating a modifier key such as SHIFT</li>
</ul>

## -see-also

<a href="/windows/desktop/api/tabflicks/ns-tabflicks-flick_data">flick_data structure</a>



<a href="/windows/desktop/tablet/flicks-gestures">flicks gestures</a>



<a href="/previous-versions/windows/desktop/ms703447(v=vs.85)">responding to pen flicks</a>



<a href="/windows/desktop/tablet/wm-tablet-flick-message">wm_tablet_flick message</a>
