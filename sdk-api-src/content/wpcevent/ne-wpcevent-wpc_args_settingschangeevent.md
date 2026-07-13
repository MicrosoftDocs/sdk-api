---
UID: NE:wpcevent.tagWPC_ARGS_SETTINGSCHANGEEVENT
title: WPC_ARGS_SETTINGSCHANGEEVENT (wpcevent.h)
description: Indicates information about the changes to settings being made by a user.
helpviewer_keywords: ["WPC_ARGS_SETTINGSCHANGEEVENT","WPC_ARGS_SETTINGSCHANGEEVENT enumeration","WPC_ARGS_SETTINGSCHANGEEVENT_CARGS","WPC_ARGS_SETTINGSCHANGEEVENT_CLASS","WPC_ARGS_SETTINGSCHANGEEVENT_NEWVAL","WPC_ARGS_SETTINGSCHANGEEVENT_OLDVAL","WPC_ARGS_SETTINGSCHANGEEVENT_OPTIONAL","WPC_ARGS_SETTINGSCHANGEEVENT_OWNER","WPC_ARGS_SETTINGSCHANGEEVENT_REASON","WPC_ARGS_SETTINGSCHANGEEVENT_SETTING","parcon.wpc_args_settingschangeevent","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_CARGS","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_CLASS","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_NEWVAL","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_OLDVAL","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_OPTIONAL","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_OWNER","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_REASON","wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_SETTING"]
old-location: parcon\wpc_args_settingschangeevent.htm
tech.root: parcon
ms.assetid: 6a933661-cf6d-4904-8e11-cd8e2bade5f0
ms.date: 12/05/2018
ms.keywords: WPC_ARGS_SETTINGSCHANGEEVENT, WPC_ARGS_SETTINGSCHANGEEVENT enumeration, WPC_ARGS_SETTINGSCHANGEEVENT_CARGS, WPC_ARGS_SETTINGSCHANGEEVENT_CLASS, WPC_ARGS_SETTINGSCHANGEEVENT_NEWVAL, WPC_ARGS_SETTINGSCHANGEEVENT_OLDVAL, WPC_ARGS_SETTINGSCHANGEEVENT_OPTIONAL, WPC_ARGS_SETTINGSCHANGEEVENT_OWNER, WPC_ARGS_SETTINGSCHANGEEVENT_REASON, WPC_ARGS_SETTINGSCHANGEEVENT_SETTING, parcon.wpc_args_settingschangeevent, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_CARGS, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_CLASS, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_NEWVAL, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_OLDVAL, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_OPTIONAL, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_OWNER, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_REASON, wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT_SETTING
req.header: wpcevent.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: WPC_ARGS_SETTINGSCHANGEEVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWPC_ARGS_SETTINGSCHANGEEVENT
 - wpcevent/tagWPC_ARGS_SETTINGSCHANGEEVENT
 - WPC_ARGS_SETTINGSCHANGEEVENT
 - wpcevent/WPC_ARGS_SETTINGSCHANGEEVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wpcevent.h
api_name:
 - WPC_ARGS_SETTINGSCHANGEEVENT
---

# WPC_ARGS_SETTINGSCHANGEEVENT enumeration


## -description

Indicates information about the changes to settings being made by a user.

## -enum-fields

### -field WPC_ARGS_SETTINGSCHANGEEVENT_CLASS:0

The class of change made to the setting.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_SETTING

The setting that was changed.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_OWNER

The user who made the change.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_OLDVAL

The previous value of the setting that was changed.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_NEWVAL

The new value of the setting that was changed.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_REASON

The reason for the changed setting.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_OPTIONAL

Optional information about the changed setting.

### -field WPC_ARGS_SETTINGSCHANGEEVENT_CARGS

The arguments of the changed setting.

