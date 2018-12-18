---
UID: NE:shobjidl_core.APPLICATION_VIEW_SIZE_PREFERENCE
title: APPLICATION_VIEW_SIZE_PREFERENCE
author: windows-sdk-content
description: Defines the set of possible general window (app view) size preferences. Used by ILaunchSourceViewSizePreference::GetSourceViewSizePreference and ILaunchTargetViewSizePreference::GetTargetViewSizePreference.
old-location: shell\APPLICATION_VIEW_SIZE_PREFERENCE.htm
tech.root: shell
ms.assetid: 20B27858-D5BC-4800-AE3F-C01A017ABBF7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: APPLICATION_VIEW_SIZE_PREFERENCE, APPLICATION_VIEW_SIZE_PREFERENCE enumeration [Windows Shell], AVSP_DEFAULT, AVSP_USE_HALF, AVSP_USE_LESS, AVSP_USE_MINIMUM, AVSP_USE_MORE, AVSP_USE_NONE, shell.APPLICATION_VIEW_SIZE_PREFERENCE, shobjidl_core/APPLICATION_VIEW_SIZE_PREFERENCE, shobjidl_core/AVSP_DEFAULT, shobjidl_core/AVSP_USE_HALF, shobjidl_core/AVSP_USE_LESS, shobjidl_core/AVSP_USE_MINIMUM, shobjidl_core/AVSP_USE_MORE, shobjidl_core/AVSP_USE_NONE
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - APPLICATION_VIEW_SIZE_PREFERENCE
product: Windows
targetos: Windows
req.typenames: APPLICATION_VIEW_SIZE_PREFERENCE
req.redist: 
---

# APPLICATION_VIEW_SIZE_PREFERENCE enumeration


## -description


Defines the set of possible general window (app view) size preferences. Used by <a href="https://msdn.microsoft.com/A151EA3D-42EE-4F22-B2A8-C696F582F81C">ILaunchSourceViewSizePreference::GetSourceViewSizePreference</a> and <a href="https://msdn.microsoft.com/2C852FD1-09FD-45B6-A493-07DEE72BEA4C">ILaunchTargetViewSizePreference::GetTargetViewSizePreference</a>.


## -enum-fields




### -field AVSP_DEFAULT

The app does not specify a window size preference. Windows, rather than the app, sets the size preference, which defaults to <b>AVSP_USE_HALF</b>.


### -field AVSP_USE_LESS

Prefers to use less than 50% of the available horizontal screen pixels.


### -field AVSP_USE_HALF

Prefers to use 50% (half) of the available horizontal screen pixels.


### -field AVSP_USE_MORE

Prefers to use more than 50% of the available horizontal screen pixels.


### -field AVSP_USE_MINIMUM

Prefers to use the minimum horizontal pixel width (either 320 or 500 pixels) specified in the app's manifest.


### -field AVSP_USE_NONE

The window has no visible component.


### -field AVSP_CUSTOM




## -see-also




<a href="https://msdn.microsoft.com/D6DF8432-7D37-4D39-9E08-2F5B874A0BCB">IApplicationDesignModeSettings2::GetApplicationViewOrientation</a>



<a href="https://msdn.microsoft.com/FCD2FDFD-1058-45D6-B9D5-A4B845CF80AA">IApplicationDesignModeSettings2::SetApplicationViewOrientation</a>
 

 

