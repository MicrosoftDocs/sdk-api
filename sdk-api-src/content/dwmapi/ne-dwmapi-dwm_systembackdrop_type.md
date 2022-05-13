---
UID: NE:dwmapi.DWM_SYSTEMBACKDROP_TYPE
title: DWM_SYSTEMBACKDROP_TYPE
description: Flags for specifying the system-drawn backdrop material of a window, including behind the non-client area.
tech.root: dwm
ms.date: 05/13/2022
req.construct-type: enumeration
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
f1_keywords:
 - DWMWINDOWATTRIBUTE
 - dwmapi/DWMWINDOWATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwmapi.h
api_name:
 - DWM_SYSTEMBACKDROP_TYPE
f1_keywords:
 - DWM_SYSTEMBACKDROP_TYPE
 - dwmapi/DWM_SYSTEMBACKDROP_TYPE
helpviewer_keywords:
 - DWM_SYSTEMBACKDROP_TYPE
prerelease: true
---

## -description

Flags for specifying the system-drawn backdrop material of a window, including behind the non-client area.

## -enum-fields

### -field DWMSBT_AUTO

The default. Let the Desktop Window Manager (DWM) automatically decide the system-drawn backdrop material for this window.

### -field DWMSBT_NONE

Don't draw any system backdrop.

### -field DWMSBT_MAINWINDOW

Draw the backdrop material effect corresponding to a long-lived window.

### -field DWMSBT_TRANSIENTWINDOW

Draw the backdrop material effect corresponding to a transient window.

### -field DWMSBT_TABBEDWINDOW

Draw the backdrop material effect corresponding to a window with a tabbed title bar.

## -remarks

## -see-also
