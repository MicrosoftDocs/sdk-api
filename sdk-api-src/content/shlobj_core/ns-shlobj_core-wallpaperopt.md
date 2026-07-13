---
UID: NS:shlobj_core._tagWALLPAPEROPT
title: WALLPAPEROPT (shlobj_core.h)
description: Contains the wallpaper display options. Used with members of the IActiveDesktop interface.
helpviewer_keywords: ["*LPWALLPAPEROPT","WALLPAPEROPT","WALLPAPEROPT structure [Windows Shell]","WPSTYLE_CENTER","WPSTYLE_CROPTOFIT","WPSTYLE_KEEPASPECT","WPSTYLE_MAX","WPSTYLE_SPAN","WPSTYLE_STRETCH","WPSTYLE_TILE","_tagWALLPAPEROPT","_win32_WALLPAPEROPT","shell.WALLPAPEROPT","shlobj_core/WALLPAPEROPT"]
old-location: shell\WALLPAPEROPT.htm
tech.root: shell
ms.assetid: 5fafbc3a-606c-4175-ac3a-132a1bfded07
ms.date: 12/05/2018
ms.keywords: '*LPWALLPAPEROPT, WALLPAPEROPT, WALLPAPEROPT structure [Windows Shell], WPSTYLE_CENTER, WPSTYLE_CROPTOFIT, WPSTYLE_KEEPASPECT, WPSTYLE_MAX, WPSTYLE_SPAN, WPSTYLE_STRETCH, WPSTYLE_TILE, _tagWALLPAPEROPT, _win32_WALLPAPEROPT, shell.WALLPAPEROPT, shlobj_core/WALLPAPEROPT'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WALLPAPEROPT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagWALLPAPEROPT
 - shlobj_core/_tagWALLPAPEROPT
 - WALLPAPEROPT
 - shlobj_core/WALLPAPEROPT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - WALLPAPEROPT
---

# WALLPAPEROPT structure


## -description

Contains the wallpaper display options. Used with members of the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop">IActiveDesktop</a> interface.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of this <b>WALLPAPEROPT</b> structure.

### -field dwStyle

Type: <b>DWORD</b>

The wallpaper style; one of the following values:



#### WPSTYLE_CENTER (0x0)

0x0. Center the wallpaper image in its original size, filling the remaining area with a solid background color if image is smaller than screen or cropping image if image is larger.



#### WPSTYLE_TILE (0x1)

0x1. Tile the wallpaper image, starting in the upper left corner of the screen. This uses the image in its original size.



#### WPSTYLE_STRETCH (0x2)

0x2. Stretch the image to cover the full screen. This can result in distortion of the image as the image's aspect ratio is not retained.



#### WPSTYLE_KEEPASPECT (0x3)

0x3. <b>Introduced in Windows 7</b>. Enlarge or shrink the image to fill the screen, retaining the aspect ratio of the original image. If necessary, the image is padded either on the top and bottom or on the right and left with the background color to fill any screen area not covered by the image.



#### WPSTYLE_CROPTOFIT (0x4)

0x4. <b>Introduced in Windows 7</b>. Enlarge or shrink the image to fill the screen, retaining the aspect ratio of the original image. If necessary, the image is cropped either on the top and bottom or on the left and right as necessary to fit the screen.



#### WPSTYLE_SPAN (0x5)

0x5. <b>Introduced in Windows 8</b>. Spans the wallpaper across multiple monitors.



#### WPSTYLE_MAX

The maximum legitimate value of these flags, used for validation purposes.
