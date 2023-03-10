---
UID: NE:dwmapi.DWM_WINDOW_CORNER_PREFERENCE
tech.root: dwm
title: DWM_WINDOW_CORNER_PREFERENCE (dwmapi.h)
description: The DWM_WINDOW_CORNER_PREFERENCE enumeration (dwmapi.h) specifies the rounded corner preference for a window.
ms.date: 08/12/2022
targetos: Windows
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: dwmapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dwmapi.h
api_name:
 - DWM_WINDOW_CORNER_PREFERENCE
f1_keywords:
 - DWM_WINDOW_CORNER_PREFERENCE
 - dwmapi/DWM_WINDOW_CORNER_PREFERENCE
dev_langs:
 - c++
---

## -description

Flags used by the <a href="nf-dwmapi-dwmsetwindowattribute.md">DwmSetWindowAttribute</a> function to specify the rounded corner preference for a window.

## -enum-fields

### -field DWMWCP_DEFAULT : 0

Let the system decide when to round window corners.

### -field DWMWCP_DONOTROUND : 1

Never round window corners.

### -field DWMWCP_ROUND : 2

Round the corners, if appropriate.

### -field DWMWCP_ROUNDSMALL : 3

Round the corners if appropriate, with a small radius.

## -remarks

## -see-also

