---
UID: NE:shobjidl_core.DESKTOP_WALLPAPER_POSITION
title: DESKTOP_WALLPAPER_POSITION (shobjidl_core.h)
description: Specifies how the desktop wallpaper should be displayed.
helpviewer_keywords: ["DESKTOP_WALLPAPER_POSITION","DESKTOP_WALLPAPER_POSITION enumeration [Windows Shell]","DWPOS_CENTER","DWPOS_FILL","DWPOS_FIT","DWPOS_SPAN","DWPOS_STRETCH","DWPOS_TILE","shell.DESKTOP_WALLPAPER_POSITION","shobjidl_core/DESKTOP_WALLPAPER_POSITION","shobjidl_core/DWPOS_CENTER","shobjidl_core/DWPOS_FILL","shobjidl_core/DWPOS_FIT","shobjidl_core/DWPOS_SPAN","shobjidl_core/DWPOS_STRETCH","shobjidl_core/DWPOS_TILE"]
old-location: shell\DESKTOP_WALLPAPER_POSITION.htm
tech.root: shell
ms.assetid: 5524E7DA-087C-475a-BB22-5E62C1A5CC4D
ms.date: 12/05/2018
ms.keywords: DESKTOP_WALLPAPER_POSITION, DESKTOP_WALLPAPER_POSITION enumeration [Windows Shell], DWPOS_CENTER, DWPOS_FILL, DWPOS_FIT, DWPOS_SPAN, DWPOS_STRETCH, DWPOS_TILE, shell.DESKTOP_WALLPAPER_POSITION, shobjidl_core/DESKTOP_WALLPAPER_POSITION, shobjidl_core/DWPOS_CENTER, shobjidl_core/DWPOS_FILL, shobjidl_core/DWPOS_FIT, shobjidl_core/DWPOS_SPAN, shobjidl_core/DWPOS_STRETCH, shobjidl_core/DWPOS_TILE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.typenames: DESKTOP_WALLPAPER_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DESKTOP_WALLPAPER_POSITION
 - shobjidl_core/DESKTOP_WALLPAPER_POSITION
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
 - DESKTOP_WALLPAPER_POSITION
---

# DESKTOP_WALLPAPER_POSITION enumeration


## -description

Specifies how the desktop wallpaper should be displayed.

## -enum-fields

### -field DWPOS_CENTER:0

Center the image; do not stretch. This is equivalent to the <a href="/windows/desktop/shell/iactivedesktop-flags">WPSTYLE_CENTER</a> style in <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>.

### -field DWPOS_TILE:1

Tile the image across all monitors. This is equivalent to the <a href="/windows/desktop/shell/iactivedesktop-flags">WPSTYLE_TILE</a> style in <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>.

### -field DWPOS_STRETCH:2

Stretch the image to exactly fit on the monitor. This is equivalent to the <a href="/windows/desktop/shell/iactivedesktop-flags">WPSTYLE_STRETCH</a> style in <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>.

### -field DWPOS_FIT:3

Stretch the image to exactly the height or width of the monitor without changing its aspect ratio or cropping the image. This can result in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getbackgroundcolor">colored letterbox bars</a> on either side or on above and below of the image. This is equivalent to the <a href="/windows/desktop/shell/iactivedesktop-flags">WPSTYLE_KEEPASPECT</a> style in <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>.

### -field DWPOS_FILL:4

Stretch the image to fill the screen, cropping the image as necessary to avoid letterbox bars. This is equivalent to the <a href="/windows/desktop/shell/iactivedesktop-flags">WPSTYLE_CROPTOFIT</a> style in <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a>.

### -field DWPOS_SPAN:5

Spans a single image across all monitors attached to the system. This flag has no <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a> equivalent.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-getposition">IDesktopWallpaper::GetPosition</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idesktopwallpaper-setposition">IDesktopWallpaper::SetPosition</a>
