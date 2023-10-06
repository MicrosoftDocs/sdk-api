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
req.target-min-winverclnt: Windows 11 Build 22621
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
prerelease: false
---

## -description

Flags for specifying the system-drawn backdrop material of a window, including behind the non-client area.

## -enum-fields

### -field DWMSBT_AUTO

The default. Let the Desktop Window Manager (DWM) automatically decide the system-drawn backdrop material for this window. This applies the backdrop material just behind the default Win32 title bar. This behavior attempts to preserve maximum backwards compatibility. For this reason, the DWM might also decide to draw no backdrop material at all based on internal heuristics.

If drawing the backdrop material behind the entire window is required, choose one of the other more specific values of this enum as appropriate.

### -field DWMSBT_NONE

Don't draw any system backdrop.

### -field DWMSBT_MAINWINDOW

Draw the backdrop material effect corresponding to a long-lived window behind the entire window bounds.

For Windows 11, this corresponds to Mica in its default variant. The material effect might change with future Windows releases. For more info about Mica, see [Mica](/windows/apps/design/style/mica).

### -field DWMSBT_TRANSIENTWINDOW

Draw the backdrop material effect corresponding to a transient window behind the entire window bounds.

For Windows 11, this corresponds to Desktop Acrylic, also known as Background Acrylic, in its brightest variant. The material effect might change with future Windows releases. For more info about Desktop Acrylic, see [Acrylic](/windows/apps/design/style/acrylic).

### -field DWMSBT_TABBEDWINDOW

Draw the backdrop material effect corresponding to a window with a tabbed title bar behind the entire window bounds.

For Windows 11, this corresponds to Mica in its alternate variant (Mica Alt). The material might change with future releases of Windows. For more info about Mica Alt, see [Layering with Mica Alt](/windows/apps/design/style/mica#app-layering-with-mica-alt).

## -remarks

## -see-also
