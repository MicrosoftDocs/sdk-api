---
UID: NE:dwmapi.DWMFLIP3DWINDOWPOLICY
title: DWMFLIP3DWINDOWPOLICY (dwmapi.h)
description: Flags used by the DwmSetWindowAttribute function to specify the Flip3D window policy.
helpviewer_keywords: ["DWMFLIP3DWINDOWPOLICY","DWMFLIP3DWINDOWPOLICY enumeration [Desktop Window Manager]","DWMFLIP3D_DEFAULT","DWMFLIP3D_EXCLUDEABOVE","DWMFLIP3D_EXCLUDEBELOW","DWMFLIP3D_LAST","_udwm_dwmflip3dwindowpolicy","_udwm_dwmflip3dwindowpolicy_cpp","dwm.dwmflip3dwindowpolicy","dwmapi/DWMFLIP3DWINDOWPOLICY","dwmapi/DWMFLIP3D_DEFAULT","dwmapi/DWMFLIP3D_EXCLUDEABOVE","dwmapi/DWMFLIP3D_EXCLUDEBELOW","dwmapi/DWMFLIP3D_LAST","winui._udwm_dwmflip3dwindowpolicy"]
old-location: dwm\dwmflip3dwindowpolicy.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\enums\dwmflip3dwindowpolicy.htm
ms.date: 12/05/2018
ms.keywords: DWMFLIP3DWINDOWPOLICY, DWMFLIP3DWINDOWPOLICY enumeration [Desktop Window Manager], DWMFLIP3D_DEFAULT, DWMFLIP3D_EXCLUDEABOVE, DWMFLIP3D_EXCLUDEBELOW, DWMFLIP3D_LAST, _udwm_dwmflip3dwindowpolicy, _udwm_dwmflip3dwindowpolicy_cpp, dwm.dwmflip3dwindowpolicy, dwmapi/DWMFLIP3DWINDOWPOLICY, dwmapi/DWMFLIP3D_DEFAULT, dwmapi/DWMFLIP3D_EXCLUDEABOVE, dwmapi/DWMFLIP3D_EXCLUDEBELOW, dwmapi/DWMFLIP3D_LAST, winui._udwm_dwmflip3dwindowpolicy
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - DWMFLIP3DWINDOWPOLICY
 - dwmapi/DWMFLIP3DWINDOWPOLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - DWMFLIP3DWINDOWPOLICY
---

# DWMFLIP3DWINDOWPOLICY enumeration


## -description

Flags used by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a> function to specify the Flip3D window policy.

## -enum-fields

### -field DWMFLIP3D_DEFAULT

Use the window's style and visibility settings to determine whether to hide or include the window in Flip3D rendering.

### -field DWMFLIP3D_EXCLUDEBELOW

Exclude the window from Flip3D and display it below the Flip3D rendering.

### -field DWMFLIP3D_EXCLUDEABOVE

Exclude the window from Flip3D and display it above the Flip3D rendering.

### -field DWMFLIP3D_LAST

The maximum recognized <a href="/windows/desktop/api/dwmapi/ne-dwmapi-dwmflip3dwindowpolicy">DWMFLIP3DWINDOWPOLICY</a> value, used for validation purposes.

## -remarks

To use a <b>DWMFLIP3DWINDOWPOLICY</b> value, set the <i>dwAttribute</i> parameter of the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a> function to <b>DWMWA_FLIP3D_POLICY</b>. Set the <i>pvAttribute</i> parameter to the <b>DWMFLIP3DWINDOWPOLICY</b> value.

## -see-also

<a href="/windows/desktop/dwm/composition-ovw">Enable and Control DWM Composition</a>