---
UID: NE:wpcevent.tagWPC_ARGS_CUSTOMEVENT
title: WPC_ARGS_CUSTOMEVENT (wpcevent.h)
description: Indicates information about a user-defined event that is not covered by the general events.
helpviewer_keywords: ["WPC_ARGS_CUSTOMEVENT","WPC_ARGS_CUSTOMEVENT enumeration","WPC_ARGS_CUSTOMEVENT_APPNAME","WPC_ARGS_CUSTOMEVENT_APPVERSION","WPC_ARGS_CUSTOMEVENT_BLOCKED","WPC_ARGS_CUSTOMEVENT_CARGS","WPC_ARGS_CUSTOMEVENT_EVENT","WPC_ARGS_CUSTOMEVENT_PUBLISHER","WPC_ARGS_CUSTOMEVENT_REASON","WPC_ARGS_CUSTOMEVENT_VALUE1","WPC_ARGS_CUSTOMEVENT_VALUE2","WPC_ARGS_CUSTOMEVENT_VALUE3","parcon.wpc_args_customevent","wpcevent/WPC_ARGS_CUSTOMEVENT","wpcevent/WPC_ARGS_CUSTOMEVENT_APPNAME","wpcevent/WPC_ARGS_CUSTOMEVENT_APPVERSION","wpcevent/WPC_ARGS_CUSTOMEVENT_BLOCKED","wpcevent/WPC_ARGS_CUSTOMEVENT_CARGS","wpcevent/WPC_ARGS_CUSTOMEVENT_EVENT","wpcevent/WPC_ARGS_CUSTOMEVENT_PUBLISHER","wpcevent/WPC_ARGS_CUSTOMEVENT_REASON","wpcevent/WPC_ARGS_CUSTOMEVENT_VALUE1","wpcevent/WPC_ARGS_CUSTOMEVENT_VALUE2","wpcevent/WPC_ARGS_CUSTOMEVENT_VALUE3"]
old-location: parcon\wpc_args_customevent.htm
tech.root: parcon
ms.assetid: 7f08d847-6042-4e56-97fd-cdf4e75da680
ms.date: 12/05/2018
ms.keywords: WPC_ARGS_CUSTOMEVENT, WPC_ARGS_CUSTOMEVENT enumeration, WPC_ARGS_CUSTOMEVENT_APPNAME, WPC_ARGS_CUSTOMEVENT_APPVERSION, WPC_ARGS_CUSTOMEVENT_BLOCKED, WPC_ARGS_CUSTOMEVENT_CARGS, WPC_ARGS_CUSTOMEVENT_EVENT, WPC_ARGS_CUSTOMEVENT_PUBLISHER, WPC_ARGS_CUSTOMEVENT_REASON, WPC_ARGS_CUSTOMEVENT_VALUE1, WPC_ARGS_CUSTOMEVENT_VALUE2, WPC_ARGS_CUSTOMEVENT_VALUE3, parcon.wpc_args_customevent, wpcevent/WPC_ARGS_CUSTOMEVENT, wpcevent/WPC_ARGS_CUSTOMEVENT_APPNAME, wpcevent/WPC_ARGS_CUSTOMEVENT_APPVERSION, wpcevent/WPC_ARGS_CUSTOMEVENT_BLOCKED, wpcevent/WPC_ARGS_CUSTOMEVENT_CARGS, wpcevent/WPC_ARGS_CUSTOMEVENT_EVENT, wpcevent/WPC_ARGS_CUSTOMEVENT_PUBLISHER, wpcevent/WPC_ARGS_CUSTOMEVENT_REASON, wpcevent/WPC_ARGS_CUSTOMEVENT_VALUE1, wpcevent/WPC_ARGS_CUSTOMEVENT_VALUE2, wpcevent/WPC_ARGS_CUSTOMEVENT_VALUE3
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
req.typenames: WPC_ARGS_CUSTOMEVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWPC_ARGS_CUSTOMEVENT
 - wpcevent/tagWPC_ARGS_CUSTOMEVENT
 - WPC_ARGS_CUSTOMEVENT
 - wpcevent/WPC_ARGS_CUSTOMEVENT
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
 - WPC_ARGS_CUSTOMEVENT
---

# WPC_ARGS_CUSTOMEVENT enumeration


## -description

Indicates information about a user-defined event that is not covered by the general events.

## -enum-fields

### -field WPC_ARGS_CUSTOMEVENT_PUBLISHER:0

The publisher of the custom event.

### -field WPC_ARGS_CUSTOMEVENT_APPNAME

The application name of the custom event.

### -field WPC_ARGS_CUSTOMEVENT_APPVERSION

The application version number of the custom event.

### -field WPC_ARGS_CUSTOMEVENT_EVENT

The type of event.

### -field WPC_ARGS_CUSTOMEVENT_VALUE1

The first  value defined for the custom event.

### -field WPC_ARGS_CUSTOMEVENT_VALUE2

The second value defined for the custom event.

### -field WPC_ARGS_CUSTOMEVENT_VALUE3

The third value defined for the custom event.

### -field WPC_ARGS_CUSTOMEVENT_BLOCKED

The custom event is blocked.

### -field WPC_ARGS_CUSTOMEVENT_REASON

The reason for the custom event.

### -field WPC_ARGS_CUSTOMEVENT_CARGS

The arguments for the custom event.

