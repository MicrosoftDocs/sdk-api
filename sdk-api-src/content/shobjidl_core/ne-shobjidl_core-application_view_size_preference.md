---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

