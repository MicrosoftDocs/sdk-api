---
UID: NE:shobjidl.UNDOCK_REASON
title: UNDOCK_REASON (shobjidl.h)
description: Values that indicate the reason that a docked accessibility app window has been undocked. Used by IAccessibilityDockingServiceCallback::Undocked.
helpviewer_keywords: ["UNDOCK_REASON","UNDOCK_REASON enumeration [Windows Shell]","UR_MONITOR_DISCONNECT","UR_RESOLUTION_CHANGE","shell.UNDOCK_REASON","shobjidl/UNDOCK_REASON","shobjidl/UR_MONITOR_DISCONNECT","shobjidl/UR_RESOLUTION_CHANGE"]
old-location: shell\UNDOCK_REASON.htm
tech.root: shell
ms.assetid: C900E0DA-C6C6-41cd-8333-38BE4D451A66
ms.date: 12/05/2018
ms.keywords: UNDOCK_REASON, UNDOCK_REASON enumeration [Windows Shell], UR_MONITOR_DISCONNECT, UR_RESOLUTION_CHANGE, shell.UNDOCK_REASON, shobjidl/UNDOCK_REASON, shobjidl/UR_MONITOR_DISCONNECT, shobjidl/UR_RESOLUTION_CHANGE
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: UNDOCK_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UNDOCK_REASON
 - shobjidl/UNDOCK_REASON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - UNDOCK_REASON
---

# UNDOCK_REASON enumeration


## -description

Values that indicate the reason that a docked accessibility app window has been undocked. Used by <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked">IAccessibilityDockingServiceCallback::Undocked</a>.

## -enum-fields

### -field UR_RESOLUTION_CHANGE:0

The accessibility window was undocked because the screen resolution has changed.

### -field UR_MONITOR_DISCONNECT:1

The monitor on which the accessibility window was docked has been disconnected.
