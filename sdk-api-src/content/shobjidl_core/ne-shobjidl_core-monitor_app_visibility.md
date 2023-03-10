---
UID: NE:shobjidl_core.MONITOR_APP_VISIBILITY
title: MONITOR_APP_VISIBILITY (shobjidl_core.h)
description: Specifies whether a display is showing desktop windows instead of Windows Store apps.
helpviewer_keywords: ["MAV_APP_VISIBLE","MAV_NO_APP_VISIBLE","MAV_UNKNOWN","MONITOR_APP_VISIBILITY","MONITOR_APP_VISIBILITY enumeration [Windows Shell]","shell.MONITOR_APP_VISIBILITY","shobjidl_core/MAV_APP_VISIBLE","shobjidl_core/MAV_NO_APP_VISIBLE","shobjidl_core/MAV_UNKNOWN","shobjidl_core/MONITOR_APP_VISIBILITY"]
old-location: shell\MONITOR_APP_VISIBILITY.htm
tech.root: shell
ms.assetid: DE52080C-5EC3-489B-ACC8-D5EAEE3DDF78
ms.date: 12/05/2018
ms.keywords: MAV_APP_VISIBLE, MAV_NO_APP_VISIBLE, MAV_UNKNOWN, MONITOR_APP_VISIBILITY, MONITOR_APP_VISIBILITY enumeration [Windows Shell], shell.MONITOR_APP_VISIBILITY, shobjidl_core/MAV_APP_VISIBLE, shobjidl_core/MAV_NO_APP_VISIBLE, shobjidl_core/MAV_UNKNOWN, shobjidl_core/MONITOR_APP_VISIBILITY
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MONITOR_APP_VISIBILITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MONITOR_APP_VISIBILITY
 - shobjidl_core/MONITOR_APP_VISIBILITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - MONITOR_APP_VISIBILITY
---

# MONITOR_APP_VISIBILITY enumeration


## -description

Specifies whether a display is showing desktop windows instead of Windows Store apps.

## -enum-fields

### -field MAV_UNKNOWN:0

The display state is not known.

### -field MAV_NO_APP_VISIBLE:1

The display is showing desktop windows.

### -field MAV_APP_VISIBLE:2

The display is not showing desktop windows.

## -remarks

The <b>MONITOR_APP_VISIBILITY</b> enum is used by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iappvisibility-getappvisibilityonmonitor">GetAppVisibilityOnMonitor</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>
