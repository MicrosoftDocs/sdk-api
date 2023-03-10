---
UID: NE:shobjidl_core.APPLICATION_VIEW_SIZE_PREFERENCE
title: APPLICATION_VIEW_SIZE_PREFERENCE (shobjidl_core.h)
description: Defines the set of possible general window (app view) size preferences. Used by ILaunchSourceViewSizePreference::GetSourceViewSizePreference and ILaunchTargetViewSizePreference::GetTargetViewSizePreference.
helpviewer_keywords: ["APPLICATION_VIEW_SIZE_PREFERENCE","APPLICATION_VIEW_SIZE_PREFERENCE enumeration [Windows Shell]","AVSP_DEFAULT","AVSP_USE_HALF","AVSP_USE_LESS","AVSP_USE_MINIMUM","AVSP_USE_MORE","AVSP_USE_NONE","shell.APPLICATION_VIEW_SIZE_PREFERENCE","shobjidl_core/APPLICATION_VIEW_SIZE_PREFERENCE","shobjidl_core/AVSP_DEFAULT","shobjidl_core/AVSP_USE_HALF","shobjidl_core/AVSP_USE_LESS","shobjidl_core/AVSP_USE_MINIMUM","shobjidl_core/AVSP_USE_MORE","shobjidl_core/AVSP_USE_NONE"]
old-location: shell\APPLICATION_VIEW_SIZE_PREFERENCE.htm
tech.root: shell
ms.assetid: 20B27858-D5BC-4800-AE3F-C01A017ABBF7
ms.date: 12/05/2018
ms.keywords: APPLICATION_VIEW_SIZE_PREFERENCE, APPLICATION_VIEW_SIZE_PREFERENCE enumeration [Windows Shell], AVSP_DEFAULT, AVSP_USE_HALF, AVSP_USE_LESS, AVSP_USE_MINIMUM, AVSP_USE_MORE, AVSP_USE_NONE, shell.APPLICATION_VIEW_SIZE_PREFERENCE, shobjidl_core/APPLICATION_VIEW_SIZE_PREFERENCE, shobjidl_core/AVSP_DEFAULT, shobjidl_core/AVSP_USE_HALF, shobjidl_core/AVSP_USE_LESS, shobjidl_core/AVSP_USE_MINIMUM, shobjidl_core/AVSP_USE_MORE, shobjidl_core/AVSP_USE_NONE
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
req.typenames: APPLICATION_VIEW_SIZE_PREFERENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPLICATION_VIEW_SIZE_PREFERENCE
 - shobjidl_core/APPLICATION_VIEW_SIZE_PREFERENCE
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
 - APPLICATION_VIEW_SIZE_PREFERENCE
---

# APPLICATION_VIEW_SIZE_PREFERENCE enumeration


## -description

Defines the set of possible general window (app view) size preferences. Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference">ILaunchSourceViewSizePreference::GetSourceViewSizePreference</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference">ILaunchTargetViewSizePreference::GetTargetViewSizePreference</a>.

## -enum-fields

### -field AVSP_DEFAULT:0

The app does not specify a window size preference. Windows, rather than the app, sets the size preference, which defaults to <b>AVSP_USE_HALF</b>.

### -field AVSP_USE_LESS:1

Prefers to use less than 50% of the available horizontal screen pixels.

### -field AVSP_USE_HALF:2

Prefers to use 50% (half) of the available horizontal screen pixels.

### -field AVSP_USE_MORE:3

Prefers to use more than 50% of the available horizontal screen pixels.

### -field AVSP_USE_MINIMUM:4

Prefers to use the minimum horizontal pixel width (either 320 or 500 pixels) specified in the app's manifest.

### -field AVSP_USE_NONE:5

The window has no visible component.

### -field AVSP_CUSTOM:6

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation">IApplicationDesignModeSettings2::GetApplicationViewOrientation</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation">IApplicationDesignModeSettings2::SetApplicationViewOrientation</a>
