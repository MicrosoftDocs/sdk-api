---
UID: NE:shobjidl_core.APPLICATION_VIEW_ORIENTATION
title: APPLICATION_VIEW_ORIENTATION (shobjidl_core.h)
description: Defines the set of display orientation modes for a window (app view). Used by IApplicationDesignModeSettings2::GetApplicationViewOrientation and IApplicationDesignModeSettings2::SetApplicationViewOrientation.
helpviewer_keywords: ["APPLICATION_VIEW_ORIENTATION","APPLICATION_VIEW_ORIENTATION enumeration [Windows Shell]","AVO_LANDSCAPE","AVO_PORTRAIT","shell.APPLICATION_VIEW_ORIENTATION","shobjidl_core/APPLICATION_VIEW_ORIENTATION","shobjidl_core/AVO_LANDSCAPE","shobjidl_core/AVO_PORTRAIT"]
old-location: shell\APPLICATION_VIEW_ORIENTATION.htm
tech.root: shell
ms.assetid: 6E14D892-09E3-46F4-84AD-991996431FB2
ms.date: 12/05/2018
ms.keywords: APPLICATION_VIEW_ORIENTATION, APPLICATION_VIEW_ORIENTATION enumeration [Windows Shell], AVO_LANDSCAPE, AVO_PORTRAIT, shell.APPLICATION_VIEW_ORIENTATION, shobjidl_core/APPLICATION_VIEW_ORIENTATION, shobjidl_core/AVO_LANDSCAPE, shobjidl_core/AVO_PORTRAIT
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: APPLICATION_VIEW_ORIENTATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPLICATION_VIEW_ORIENTATION
 - shobjidl_core/APPLICATION_VIEW_ORIENTATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - APPLICATION_VIEW_ORIENTATION
---

# APPLICATION_VIEW_ORIENTATION enumeration


## -description

Defines the set of display orientation modes for a window (app view). Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation">IApplicationDesignModeSettings2::GetApplicationViewOrientation</a> and 
            <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation">IApplicationDesignModeSettings2::SetApplicationViewOrientation</a>.

## -enum-fields

### -field AVO_LANDSCAPE:0

The window is in landscape orientation, with the display width greater than the height.

### -field AVO_PORTRAIT

The window is in portrait orientation, with the display height greater than the width.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation">IApplicationDesignModeSettings2::GetApplicationViewOrientation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation">IApplicationDesignModeSettings2::SetApplicationViewOrientation</a>
