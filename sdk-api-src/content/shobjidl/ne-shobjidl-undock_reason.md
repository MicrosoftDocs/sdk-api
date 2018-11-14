---
UID: NE:shobjidl.UNDOCK_REASON
title: UNDOCK_REASON
author: windows-sdk-content
description: Values that indicate the reason that a docked accessibility app window has been undocked. Used by IAccessibilityDockingServiceCallback::Undocked.
old-location: shell\UNDOCK_REASON.htm
tech.root: shell
ms.assetid: C900E0DA-C6C6-41cd-8333-38BE4D451A66
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: UNDOCK_REASON, UNDOCK_REASON enumeration [Windows Shell], UR_MONITOR_DISCONNECT, UR_RESOLUTION_CHANGE, shell.UNDOCK_REASON, shobjidl/UNDOCK_REASON, shobjidl/UR_MONITOR_DISCONNECT, shobjidl/UR_RESOLUTION_CHANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - UNDOCK_REASON
product: Windows
targetos: Windows
req.typenames: UNDOCK_REASON
req.redist: 
---

# UNDOCK_REASON enumeration


## -description


Values that indicate the reason that a docked accessibility app window has been undocked. Used by <a href="https://msdn.microsoft.com/AFD60F5B-3017-49a2-8AFC-8309D11B3ACA">IAccessibilityDockingServiceCallback::Undocked</a>.


## -enum-fields




### -field UR_RESOLUTION_CHANGE

The accessibility window was undocked because the screen resolution has changed.


### -field UR_MONITOR_DISCONNECT

The monitor on which the accessibility window was docked has been disconnected.

