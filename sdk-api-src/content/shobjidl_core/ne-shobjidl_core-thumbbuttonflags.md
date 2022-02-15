---
UID: NE:shobjidl_core.THUMBBUTTONFLAGS
title: THUMBBUTTONFLAGS (shobjidl_core.h)
description: Used by THUMBBUTTON to control specific states and behaviors of the button.
helpviewer_keywords: ["THBF_DISABLED","THBF_DISMISSONCLICK","THBF_ENABLED","THBF_HIDDEN","THBF_NOBACKGROUND","THBF_NONINTERACTIVE","THUMBBUTTONFLAGS","THUMBBUTTONFLAGS enumeration [Windows Shell]","_shell_THUMBBUTTONFLAGS","shell.THUMBBUTTONFLAGS","shobjidl_core/THBF_DISABLED","shobjidl_core/THBF_DISMISSONCLICK","shobjidl_core/THBF_ENABLED","shobjidl_core/THBF_HIDDEN","shobjidl_core/THBF_NOBACKGROUND","shobjidl_core/THBF_NONINTERACTIVE","shobjidl_core/THUMBBUTTONFLAGS"]
old-location: shell\THUMBBUTTONFLAGS.htm
tech.root: shell
ms.assetid: 601a2517-cfce-4edb-b2ca-e2ed8a365a0d
ms.date: 12/05/2018
ms.keywords: THBF_DISABLED, THBF_DISMISSONCLICK, THBF_ENABLED, THBF_HIDDEN, THBF_NOBACKGROUND, THBF_NONINTERACTIVE, THUMBBUTTONFLAGS, THUMBBUTTONFLAGS enumeration [Windows Shell], _shell_THUMBBUTTONFLAGS, shell.THUMBBUTTONFLAGS, shobjidl_core/THBF_DISABLED, shobjidl_core/THBF_DISMISSONCLICK, shobjidl_core/THBF_ENABLED, shobjidl_core/THBF_HIDDEN, shobjidl_core/THBF_NOBACKGROUND, shobjidl_core/THBF_NONINTERACTIVE, shobjidl_core/THUMBBUTTONFLAGS
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: THUMBBUTTONFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - THUMBBUTTONFLAGS
 - shobjidl_core/THUMBBUTTONFLAGS
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
 - THUMBBUTTONFLAGS
---

# THUMBBUTTONFLAGS enumeration


## -description

Used by <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-thumbbutton">THUMBBUTTON</a> to control specific states and behaviors of the button.

## -enum-fields

### -field THBF_ENABLED:0

The button is active and available to the user.

### -field THBF_DISABLED:0x1

The button is disabled. It is present, but has a visual state that indicates that it will not respond to user action.

### -field THBF_DISMISSONCLICK:0x2

When the button is clicked, the taskbar button's flyout closes immediately.

### -field THBF_NOBACKGROUND:0x4

Do not draw a button border, use only the image.

### -field THBF_HIDDEN:0x8

The button is not shown to the user.

### -field THBF_NONINTERACTIVE:0x10

The button is enabled but not interactive; no pressed button state is drawn. This value is intended for instances where the button is used in a notification.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-thumbbutton">THUMBBUTTON</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask">THUMBBUTTONMASK</a>
