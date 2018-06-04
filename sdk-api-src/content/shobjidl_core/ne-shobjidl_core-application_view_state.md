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

# APPLICATION_VIEW_STATE enumeration


## -description


Indicates the current view state of a Windows Store app. Used by <a href="https://msdn.microsoft.com/37e1845c-a58a-4da3-b259-bbf5bbf5ff6d">IApplicationDesignModeSettings::SetApplicationViewState</a> and <a href="https://msdn.microsoft.com/49661f00-15bc-48c0-a302-b81bee61180a">IApplicationDesignModeSettings::IsApplicationViewStateSupported</a>.


## -enum-fields




### -field AVS_FULLSCREEN_LANDSCAPE

The current app's view is full-screen (has no snapped app adjacent to it), and is in landscape orientation.


### -field AVS_FILLED

The current app's view has been reduced to a partial screen view as the result of another app snapping (being docked at one side of the screen in a narrow view).


### -field AVS_SNAPPED

The current app's view has been snapped (docked at one side of the screen in a narrow view).


### -field AVS_FULLSCREEN_PORTRAIT

The current app's view is full-screen (has no snapped app adjacent to it), and is in portrait orientation.


## -see-also




<a href="https://msdn.microsoft.com/49661f00-15bc-48c0-a302-b81bee61180a">IApplicationDesignModeSettings::IsApplicationViewStateSupported</a>



<a href="https://msdn.microsoft.com/37e1845c-a58a-4da3-b259-bbf5bbf5ff6d">IApplicationDesignModeSettings::SetApplicationViewState</a>
 

 

