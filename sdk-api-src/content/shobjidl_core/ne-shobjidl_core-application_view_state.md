---
UID: NE:shobjidl_core.APPLICATION_VIEW_STATE
title: APPLICATION_VIEW_STATE
author: windows-sdk-content
description: Indicates the current view state of a Windows Store app. Used by IApplicationDesignModeSettings::SetApplicationViewState and IApplicationDesignModeSettings::IsApplicationViewStateSupported.
old-location: shell\APPLICATION_VIEW_STATE.htm
old-project: shell
ms.assetid: A79F66BD-2972-4f30-9284-E88B8201F38D
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: APPLICATION_VIEW_STATE, APPLICATION_VIEW_STATE enumeration [Windows Shell], AVS_FILLED, AVS_FULLSCREEN_LANDSCAPE, AVS_FULLSCREEN_PORTRAIT, AVS_SNAPPED, shell.APPLICATION_VIEW_STATE, shobjidl_core/APPLICATION_VIEW_STATE, shobjidl_core/AVS_FILLED, shobjidl_core/AVS_FULLSCREEN_LANDSCAPE, shobjidl_core/AVS_FULLSCREEN_PORTRAIT, shobjidl_core/AVS_SNAPPED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPLICATION_VIEW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - APPLICATION_VIEW_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
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
 

 

